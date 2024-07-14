# Vehicle Price Estimation API

## Overview
The Vehicle Price Estimation API is a powerful and scalable application built using NestJS and TypeORM. This API is designed to provide users with accurate price estimates for vehicles based on various parameters such as make, model, year, mileage, and geographic location.

## Features
- **User Authentication and Authorization**
  - Secure user authentication using sessions.
  - Role-based access control to protect sensitive endpoints.

- **Vehicle Reports Management**
  - Create, read, update, and delete vehicle reports.
  - Store detailed information about each vehicle, including make, model, year, mileage, location, and price.

- **Price Estimation**
  - Advanced price estimation algorithm based on historical data and market trends.
  - Query endpoints to retrieve average price estimates for vehicles based on user-provided criteria.

- **Data Validation and Serialization**
  - Use of DTOs (Data Transfer Objects) for validating and transforming input data.
  - Custom serialization to control the data format sent to the clients.

- **Database Integration**
  - Integration with SQLite for development and testing environments.
  - PostgreSQL support for production with seamless migration management using TypeORM.

- **Modular Architecture**
  - Clean and maintainable codebase with a modular structure.
  - Easy to extend and add new features.

- **Error Handling and Logging**
  - Centralized error handling for consistent error responses.
  - Comprehensive logging to track application activity and errors.

## Technology Stack
- **Backend Framework**: NestJS
- **ORM**: TypeORM
- **Database**: SQLite (development and testing), PostgreSQL (production)
- **Authentication**: Sessions
- **Validation**: Class-validator
- **Serialization**: Class-transformer
- **Language**: TypeScript

## Installation and Setup
1. **Clone the Repository**:
    ```bash
    git clone https://github.com/Keshav0907/Vehicle-Price-Estimation-API.git
    cd vehicle-price-estimation-api
    ```

2. **Install Dependencies**:
    ```bash
    npm install
    ```

3. **Set Up Environment Variables**:
    Create a `.env` file in the root directory and configure your environment variables.
    ```env
    NODE_ENV=development
    DB_TYPE=sqlite
    DB_NAME=db.sqlite
    ```

4. **Run Migrations**:
    ```bash
    npm run typeorm migration:run
    ```

5. **Start the Application**:
    ```bash
    npm run start:dev
    ```

## Usage
### Authentication
- **Register a new user**: `POST /auth/register`
- **Login**: `POST /auth/login`

### Vehicle Reports
- **Create a report**: `POST /reports`
- **Get all reports**: `GET /reports`
- **Get a report by ID**: `GET /reports/:id`
- **Update a report**: `PATCH /reports/:id`
- **Delete a report**: `DELETE /reports/:id`

### Price Estimation
- **Get price estimate**: `GET /estimates?make=MAKE&model=MODEL&year=YEAR&mileage=MILEAGE&lng=LNG&lat=LAT`


