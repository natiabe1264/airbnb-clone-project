# 🏡 Airbnb Clone Backend – ProDev Project

## 📌 Overview

This project is a backend-focused clone of Airbnb, designed as part of the **ProDev Backend Program** to simulate building a scalable, secure booking platform. It mimics real-world engineering workflows and emphasizes backend systems, database design, CI/CD, and team collaboration.

## 🎯 Project Goals

The goal of this project is to develop a full-featured backend system that supports core functionalities of a booking platform, including user management, property listings, availability tracking, secure API endpoints, and automated deployment pipelines. It also aims to foster collaboration through version control, documentation, and team role clarity.

## 👥 Team Roles

The development of the Airbnb Clone backend involves a collaborative effort from various technical roles, each contributing to a key part of the system's success.

### 🔧 Backend Developer
Responsible for building the core application logic and RESTful/GraphQL APIs. Implements features such as user authentication, property management, bookings, and reviews. Ensures code quality, scalability, and security best practices are followed.

### 🗄️ Database Administrator (DBA)
Designs and manages the PostgreSQL database schema. Optimizes data storage, indexing, and query performance. Works closely with backend developers to ensure data integrity and efficient data access.

### ⚙️ DevOps Engineer
Handles deployment infrastructure, including Docker and CI/CD pipelines. Ensures the backend runs reliably in development and production environments. Sets up monitoring, logging, and automated testing workflows using tools like GitHub Actions.

### 🧪 QA Engineer
Tests the backend features and APIs to ensure they meet functional and performance requirements. Writes test cases, runs integration tests, and reports bugs. Validates user flows such as booking, payments, and authentication.



## 🛠️ Technology Stack

This project uses a combination of modern backend technologies to simulate a real-world booking platform like Airbnb. Below is an overview of each tool and its role in the system:

- **Django**: A powerful Python-based web framework used to build the core backend logic, define models, and implement RESTful APIs.

- **MySQL**: A relational database management system used to store and manage structured data, including users, listings, bookings, and transactions.

- **GraphQL**: An API query language that enables precise and efficient data fetching, giving clients control over the structure and size of the responses.

- **Docker**: A containerization tool that packages the application and its dependencies into isolated environments, making it easy to run consistently across different systems.

- **Git & GitHub**: Tools for version control and collaboration, allowing the team to manage source code, track changes, and coordinate development workflows.

- **GitHub Actions**: A CI/CD automation tool used to build, test, and deploy the application, ensuring smooth and consistent integration and delivery.

- **Markdown**: A markup language used to format documentation like the `README.md` file, making it clear and readable for developers and contributors.

## 🗃️ Database Design

The Airbnb Clone backend relies on a well-structured relational database to support essential features such as user management, property listings, bookings, payments, and reviews. Below is an overview of the core entities and their relationships.

### 🧑 Users
Stores information about guests and hosts.
- `id`: Primary key
- `name`: Full name of the user
- `email`: Unique email for authentication
- `password_hash`: Encrypted password
- `is_host`: Boolean flag to distinguish between guests and hosts

### 🏡 Properties
Represents accommodations listed by hosts.
- `id`: Primary key
- `title`: Name or title of the property
- `description`: Property details
- `location`: Address or geolocation
- `owner_id`: Foreign key to `Users`

### 📅 Bookings
Tracks reservation information for properties.
- `id`: Primary key
- `user_id`: Foreign key to `Users` (the guest)
- `property_id`: Foreign key to `Properties`
- `start_date`: Check-in date
- `end_date`: Check-out date

### 💵 Payments
Handles payment transactions for bookings.
- `id`: Primary key
- `booking_id`: Foreign key to `Bookings`
- `amount`: Total payment amount
- `payment_status`: Enum or string (e.g., pending, completed, failed)
- `payment_date`: Timestamp of transaction

### 🌟 Reviews
Allows users to rate and review properties.
- `id`: Primary key
- `user_id`: Foreign key to `Users`
- `property_id`: Foreign key to `Properties`
- `rating`: Integer or decimal score
- `comment`: Text review

### 🔗 Entity Relationships
- A **user** can be both a **host** (owning properties) and a **guest** (making bookings).
- A **property** belongs to one **user** (host) but can have many **bookings** and **reviews**.
- A **booking** is made by a **user** for a **property**.
- A **payment** is linked to a **booking**.
- A **review** is written by a **user** for a **property**.

## ✨ Feature Breakdown

This section outlines the core features of the Airbnb Clone project and their role in delivering a robust booking platform.

### 👤 User Management
Handles registration, authentication, and profile management for users. This feature ensures secure access to the platform and differentiates between guests and hosts.

### 🏘️ Property Management
Allows hosts to create, update, and manage their property listings. Each property includes details such as location, description, pricing, and availability.

### 📆 Booking System
Enables guests to browse available properties, make reservations, and manage booking details. This feature supports check-in/check-out tracking and prevents scheduling conflicts.

### 💳 Payment Processing
Processes transactions related to bookings, ensuring secure and accurate payment handling. This includes tracking payment status and recording transaction data.

### ⭐ Review System
Allows guests to leave feedback on their stays by submitting reviews and ratings. This builds trust and transparency between users and hosts.

### 📚 API Documentation
Provides clear, standardized documentation for all REST and GraphQL API endpoints using the OpenAPI standard. This improves usability and integration for frontend and third-party developers.

### ⚙️ Data Optimization
Implements indexing and caching strategies to enhance performance and reduce server load. This ensures smooth and efficient data retrieval across the application.

---

## 🔍 Key Features

- Modular codebase structured for scalability
- Secure authentication and authorization
- Well-documented GitHub repository and README
- CI/CD integration for streamlined development
- Real-world database modeling and relationships
