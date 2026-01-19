FROM ruby:3.1.2

# Install dependencies
RUN apt-get update -qq && apt-get install -y nodejs postgresql-client

# Set working directory
WORKDIR /app

# Copy Gemfiles
COPY Gemfile Gemfile.lock ./

# Install gems
RUN bundle install

# Copy rest of the app
COPY . .

# Precompile assets (optional for API-only apps)
# RUN bundle exec rake assets:precompile

# Start the serverCMD
CMD ["bash", "-c", "rm -f tmp/pids/server.pid && bundle exec rails server -b 0.0.0.0 -p 8000"]
