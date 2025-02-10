# Banking Application

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Prerequisites](#prerequisites)
- [Setup Instructions](#setup-instructions)
  - [1. Clone the Repository](#1-clone-the-repository)
  - [2. Navigate to the project directory](#2-Navigate-to-the-project-directory)
  - [3. Configure Database](#3-configure-database)
  - [4. Build and Run the Application](#4-build-and-run-the-application)
  - [5. Access the Application](#5-access-the-application)
- [Project Structure](#project-structure)
- [API Endpoints](#api-endpoints)
- [Security](#security)
- [Future Enhancements](#future-enhancements)
- [Screenshots](#screenshots)

## Overview
This is a web-based Banking Application built using **Spring Boot**, **Thymeleaf**, **MySQL**, and **Java**. The application provides essential banking functionalities such as user authentication, account management, transactions, and balance inquiry.

## Features
- User authentication (Login & Registration)
- Account management (View account details, update profile)
- Fund transfer between accounts
- Transaction history
- Deposit and withdrawal functionality
- Admin dashboard to manage users and accounts

## Tech Stack
- **Backend:** Spring Boot, Java
- **Frontend:** Thymeleaf, HTML, CSS, JavaScript
- **Database:** MySQL
- **ORM:** Hibernate (JPA)

## Prerequisites
Ensure you have the following installed before running the application:
- Java (JDK 17 or later)
- MySQL Server
- Maven
- Spring Boot

## Setup Instructions

### 1. Clone the Repository
    ```bash
    git clone https://github.com/thilaksagarn/bankapp.git
### 2. Navigate to the project directory:
    ```bash
    cd bankapp
### 3. Configure Database

1. **Create a MySQL Database**  
   Create a MySQL database named `bankappdb` by running the following SQL command in your MySQL console or GUI tool:
   ```sql
   CREATE DATABASE bankappdb;
2. **Update Application Properties**
   Update the src/main/resources/application.properties file with your MySQL credentials. Replace yourpassword with your actual MySQL password:
   spring.datasource.url=jdbc:mysql://localhost:3306/bankappdb
   spring.datasource.username=root
   spring.datasource.password=yourpassword
   spring.jpa.hibernate.ddl-auto=update
### 4. Build and Run the Application
    ```bash
    mvn clean install
    mvn spring-boot:run
### 5. Access the Application
    Once the application starts, open your browser and go to:
    http://localhost:8080

## 6. Project Structure
    ```bash
    📂 bankapp
    ├── 📂 src/main/java/com/bankingapp
    │   ├── 📂 controller       # Handles HTTP requests
    │   ├── 📂 model            # Entity classes for database
    │   ├── 📂 repository       # Data access layer (Spring Data JPA)
    │   ├── 📂 service          # Business logic layer
    │   ├── 📂 config           # Security and configuration classes
    ├── 📂 src/main/resources/templates  # Thymeleaf HTML templates
    ├── 📂 src/main/resources/static      # CSS, JS, images
    ├── 📜 application.properties
    ├── 📜 pom.xml (Maven dependencies)
## API Endpoints

Below is a list of the available API endpoints and their descriptions:

| Endpoint         | Method | Description                     |
|------------------|--------|---------------------------------|
| `/`              | GET    | Home page                       |
| `/login`         | GET    | User login page                 |
| `/register`      | GET    | User registration page          |
| `/dashboard`     | GET    | User dashboard                  |
| `/transactions`  | GET    | View transaction history        |

## Security

The application uses **Spring Security** for authentication and authorization:
- Passwords are securely hashed using **BCrypt** to ensure data protection.
- Role-based access control ensures that only authorized users can access specific endpoints (e.g., `ADMIN` for the admin dashboard).
- CSRF protection is enabled to prevent cross-site request forgery attacks.
- Session management is configured to handle user sessions securely.

## Future Enhancements

Below are some planned features and enhancements for the application:
- **Two-Factor Authentication (2FA):** Add an extra layer of security for user accounts.
- **Notification System:** Implement real-time notifications for transactions and account activities.
- **Mobile Banking API:** Introduce a RESTful API to support mobile banking applications.
## Screenshots
 ![Screenshot 2025-02-10 214026](https://github.com/user-attachments/assets/43ba790d-d6b3-4602-bf17-9aaef49b77ef)
 ![Screenshot 2025-02-10 214005](https://github.com/user-attachments/assets/e73e1928-6fc6-4c6f-913b-b06a9ee53553)
 ![Screenshot 2025-02-10 214114](https://github.com/user-attachments/assets/c18a3dfb-ce76-4755-8602-2fd4bda4ee6f)
 ![Screenshot 2025-02-10 214134](https://github.com/user-attachments/assets/9c351f59-15c4-4d74-899f-5d9852079642)




