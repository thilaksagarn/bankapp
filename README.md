# Banking Application

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
cd bankapp

## Configure Database
### Create a MySQL database named bankappdb.
### Update src/main/resources/application.properties with your MySQL credentials:
