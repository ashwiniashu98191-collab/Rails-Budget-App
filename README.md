# Rails-Budget-App

The repository is a simple budget management app built with Ruby on Rails, designed to let users manage categories (like groceries or bills) and records. It uses PostgreSQL for data storage and is containerized with Docker and Docker Compose.

# Steps to run

used wsl(ubuntu) to dockerize.

## Clone the repository

git clone https://github.com/evans22j/Budget-App

cd Budget-App

git checkout app

## Run the App

docker-compose build

docker-compose run web rails db:create db:migrate

docker-compose up

## Create the admin user
docker-compose run web rails console

User.create!(name: "Admin User", email: "admin@example.com", password: "password123", password_confirmation: "password123")

## Visit the app at

http://localhost:8000
