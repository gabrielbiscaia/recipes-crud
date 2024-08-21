# NestJS CRUD REST API with Docker, Swagger, and Prisma

This project is a CRUD (Create, Read, Update, Delete) REST API built with NestJS, Docker, Swagger, and Prisma. It demonstrates how to create a robust and scalable API using modern web development technologies.

## Features

- NestJS framework for building efficient and scalable server-side applications
- PostgreSQL database
- Prisma as the ORM for database operations
- Docker for containerization and easy deployment
- Swagger for API documentation
- CRUD operations for managing recipes

## Prerequisites

Before you begin, ensure you have the following installed on your local machine:

- Node.js (v14 or later)
- npm (comes with Node.js)
- Docker and Docker Compose
- Git

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/gabrielbiscaia/crud-recipes.git
   cd crud-recipes
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
   npx prisma migrate dev
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

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License.