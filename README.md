# TReviewer

## Table of Contents
- [Short Description of the App](#short-description-of-the-app)
- [Installation Guide](#installation-guide)
- [Features](#features)

## Short Description of the App

TReviewer is a web application that allows users to share opinions about railway stations and train connections offered by railway operators as well as airlines. This is a basic app that doesn't implement many quality of life features that are usually added to modern apps. Front End was made with mobile users in mind.

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

<img width="802" height="512" alt="obraz" src="https://github.com/user-attachments/assets/3ea1e100-7896-484a-b835-d8868a52ab06" />

### User Login

<img width="775" height="478" alt="obraz" src="https://github.com/user-attachments/assets/d09650fa-77be-4701-847b-c0e17319b967" />

### Railway Station Reviews

<img width="1880" height="536" alt="obraz" src="https://github.com/user-attachments/assets/dff87e52-c06c-49ef-bc9a-7d7cc649393a" />

### Train Connection Reviews

<img width="1867" height="314" alt="obraz" src="https://github.com/user-attachments/assets/8f6fc3a4-58d3-4680-b5b5-26c784c7d17e" />

### Search

<img width="784" height="555" alt="obraz" src="https://github.com/user-attachments/assets/5f8a81aa-dfb5-4de0-8e40-fe82c7b243a8" />

### Adding a review

<img width="1296" height="491" alt="obraz" src="https://github.com/user-attachments/assets/aee58f91-3f73-43f4-a8ec-6dc1029d3bb1" />
