# Laravel Application Boilerplate

This Laravel application boilerplate is designed to kickstart your development process. It comes with an out-of-the-box Nginx configuration, Dockerized environments including PostgreSQL and RabbitMQ services, and a ready-to-go structured Dockerfile and docker-compose.yaml file.

## Prerequisites

Before you begin, ensure you have the following installed on your system:
- Docker Desktop
- Composer
- Git

## Setup Instructions

Follow these steps to get your development environment up and running:

## 1. Clone the Project

Clone this repository to your local machine using Git:

```bash
git clone https://github.com/Tope19/docker-nginx-laravel-boilerplate.git
```

## 2. Install Dependencies
Navigate to the cloned directory and install PHP dependencies with Composer:

```bash 
composer install
```

## 3. Environment Configuration
Copy the example environment file to create your own .env file:

```bash
cp .env.example .env
```

Adjust the database and RabbitMQ credentials in your .env file to your preferred settings. Ensure these credentials match the ones defined in your docker-compose.yaml file.

## 4. Start Docker Desktop
Ensure your Docker Desktop application is running before proceeding to the next steps.

## 5. Build and Run Containers
Build and start the Docker containers in detached mode:

```bash
docker-compose up --build -d
```

## 6. Database Migrations
To migrate your database, first, find the container ID of your Laravel application:

```bash
docker ps
```

Then, execute the Laravel migration command within your Docker container:

```bash
docker exec <containerId> php artisan migrate
```

Replace <containerId> with your actual Laravel application container ID.

You can follow this pattern to run other php artisan commands within your Docker container.

## Usage
After completing the setup instructions, your Laravel application should be up and running within Docker containers, accessible via the configured ports.

## Contributing
We welcome contributions! Please feel free to submit pull requests to the repository.
