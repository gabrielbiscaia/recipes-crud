# Recipes CRUD

## Objective
Create a CRUD (Create, Read, Update, Delete) using NestJS, Docker, Swagger, and Prisma, that allows users to manage recipes.

## Technologies

- NestJS framework for building server-side applications
- PostgreSQL for database
- Prisma as the ORM
- Docker for containerization and easy deployment
- Swagger for API documentation
- CRUD operations for managing recipes

## Prerequisites

Before you begin, ensure you have the following installed on your local machine:

- Node.js (v14 or later)
- npm (comes with Node.js)
- Docker and Docker Compose
- Git

## Settings
To run the application, you need to put in the .env file the following variables:
```
### PostgreSQL
DATABASE_URL='YOUR_DATABASE_URL'
```

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/gabrielbiscaia/recipes-crud/.git
   cd recipes-crud/
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up your environment variables:
   ```bash
   cp .env.example .env
   ```
   Edit the `.env` file with your database credentials and other configurations.

4. Start the PostgreSQL database using Docker:
   ```bash
   docker-compose up -d
   ```

5. Run Prisma migrations:
   ```bash
   npx prisma db push
   ```

6. Generate Prisma client:
   ```bash
   npx prisma generate
   ```

## Running the Application

1. Start the NestJS application:
   ```bash
   npm run start:dev
   ```

2. The API will be available at `http://localhost:3000`

3. Access the Swagger documentation at `http://localhost:3000/api`

## API Endpoints

- `GET /recipes`: Fetch all recipes
- `GET /recipes/:id`: Fetch a single recipe by ID
- `POST /recipes`: Create a new recipe
- `PATCH /recipes/:id`: Update an existing recipe
- `DELETE /recipes/:id`: Delete a recipe

For detailed information about request/response formats, please refer to the Swagger documentation.

## Testing

To run the tests:

```bash
npm run test
```
