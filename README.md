
![Current Status](https://github.com/perry-walid/employee_directory/actions/workflows/github-actions-demo.yml/badge.svg)

# Employee Directory: Your Essential HR Tool

Welcome to the Employee Directory repository! This Rails application is designed to simplify human resource management for businesses of all sizes by providing a robust platform to manage employee records, communications, and reporting.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Docker: Installed and running
- Ruby: Version 3.2.3 (for local development without Docker)
- Node.js: Installed (for local development without Docker)
- Yarn: Installed (for local development without Docker)
- PostgreSQL: Installed and running (for local development without Docker)
- Rails 7.1.3.4 (for local development without Docker)

## Installation
### Using Docker

1. Clone the Repository

```bash
git clone https://github.com/perry-walid/employee-directory.git
cd employee-directory
```

2. Create and Start Containers

```bash
docker-compose build --no-cache
docker-compose up
```

This command will:

- Build the Docker images for the application and the database.
- Create and start the containers.

3. Set up the Database

Open a new terminal and run the following command to set up the database:

```bash
docker-compose run web rake db:create db:migrate db:seed
```

4. Access the Application:

The application should now be running at `http://localhost:3000`.

### Running Locally (Without Docker)

1. Clone the Repository:

```bash
git clone https://github.com/perry-walid/employee-directory.git
cd employee-directory
```

2. Install Dependencies:

```bash
bundle install
```

3. Set Up the Database:

Ensure PostgreSQL is running, then run:

```bash
rake db:create db:migrate db:seed
```

4. Start the Rails Server:

```bash
rails server
```

The application should now be running at http://localhost:3000.

## Additional Information
- Health Check: You can check the health status of the application by accessing the /health endpoint. This will return a 200 status code if the app is running without exceptions, otherwise 500.

```bash
GET /health
```

- API Documentation: You can view all exposed endpoints by accessing the /api/v1/vandal endpoint. This provides a comprehensive list of all API endpoints available in the application.

```bash
GET /api/v1/vandal/
```