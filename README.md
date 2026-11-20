# TReviewer

## Table of Contents
- [Short Description of the App](#short-description-of-the-app)
- [Installation Guide](#installation-guide)
- [Features](#features)

## Short Description of the App

TReviewer is a web application that allows users to share opinions about railway stations and train connections offered by railway operators.

## Installation Guide

### Requirements
- Java 17
- Maven
- PostgreSQL
- Node.js and npm

### PostgreSQL Setup

Create a PostgreSQL database and user:

```sql
CREATE ROLE admin WITH LOGIN PASSWORD '{password}';
CREATE DATABASE {database_name} OWNER {database_owner};
```

Update the database settings in `backend/Treviewer/src/main/resources/application.properties` if needed:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/{database name}
spring.datasource.username={database owner}
spring.datasource.password={password}
```

The application uses JPA with `spring.jpa.hibernate.ddl-auto=update`, so tables are generated automatically when the backend starts.

### Start the Backend

```bash
cd backend/Treviewer
./mvnw spring-boot:run
```

On Windows:

```bash
mvnw.cmd spring-boot:run
```

### Start the Frontend

In a second terminal:

```bash
cd frontend
npm install
npm start
```

Open `http://localhost:3000` in your browser.

## Features

### User Registration
![Screenshot placeholder — user registration](./screenshots/user-registration.png)

### User Login
![Screenshot placeholder — user login](./screenshots/user-login.png)

### Railway Station Reviews
![Screenshot placeholder — railway station reviews](./screenshots/station-reviews.png)

### Train Connection Reviews
![Screenshot placeholder — train connection reviews](./screenshots/route-reviews.png)

### Search
![Screenshot placeholder — search](./screenshots/search.png)

### Favorite Stations
![Screenshot placeholder — favorite stations](./screenshots/favorite-stations.png)
