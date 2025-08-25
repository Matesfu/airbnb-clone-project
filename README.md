# airbnb-clone-project
## About The Project
> The Airbnb Clone Project is a real-world web application designed to simulate a scalable booking platform like Airbnb. The project focuses on backend development, database design, API creation, and application security, enable to understand complex architectures, workflows, and team collaboration.
### Project Goals:
* Build a robust backend system capable of handling user authentication, property listings, bookings, and reviews.<br>
* Design a relational database that efficiently manages data integrity and relationships.<br>
* Implement secure APIs and understand best practices for application security.<br>
* Integrate CI/CD pipelines to automate testing, deployment, and development workflows.<br>
## Team Roles
### Backend Developer 
Responsible for designing, developing, and maintaining the server-side logic of the application. Key responsibilities include:
* Building RESTful APIs using Django.<br>
* Implementing security measures to protect user data and transactions.<br>
* Developing and maintaining CI/CD pipelines for automated testing and deployment.<br>  
### Database Administrator
Responsible for managing the database and ensuring data integrity, performance, and security. Key responsibilities include:
* Designing and maintaining the PostgreSQL database schema.<br>
* Managing data storage, backups, and recovery.<br>
* Monitoring and optimizing database performance for efficient queries. <br>
## Technology Stack
* Django: a web framework for building RESTful APIs, user authentication, booking management, and server-side logic.  
* PostgreSQL: A powerful, open-source relational database used to store all the application data.

## Database Design
The database is designed using PostgreSQL to ensure data integrity and support complex relationships. Below are the key entities and their fields:
### Entities & Fields
#### 1. Users
* id (Primary Key)
* name (Full name of the user)
* email (Unique email for login)
* password_hash (Encrypted password)
* role (e.g., host, guest)
#### 2. Properties
* id (Primary Key)
* title (Property name)
* description (Details of the property)
* price
* owner_id (Foreign Key referencing Users)
#### 3. Bookings
* id (Primary Key)
* property_id (Foreign Key referencing Properties)
* user_id (Foreign Key referencing Users)
* check_in_date
* check_out_date
#### 4. Reviews
* id (Primary Key)
* property_id (Foreign Key referencing Properties)
* user_id (Foreign Key referencing Users)
* rating (1-5 scale)
* comment
#### 5. Payments
* id (Primary Key)
* booking_id (Foreign Key referencing Bookings)
* amount
* payment_status (e.g., pending, completed)
### Relationships
* A User can have multiple Properties (One-to-Many).
* A User can make multiple Bookings (One-to-Many).
* A Property can have multiple Bookings and Reviews (One-to-Many).
* A Booking belongs to one Property and one User (Many-to-One).
* A Payment is linked to one Booking (One-to-One).
## Feature Breakdown
### 1. User Management
Allows users to register, log in, and manage their profiles. This feature ensures secure authentication, role-based access (e.g., guest or host), and provides a personalized experience for each user.
###2. Property Management
Enables hosts to create, update, and delete property listings. Users can browse detailed property information, including descriptions, photos, pricing, and availability, making it easy to manage and showcase listings.
### 3. Booking System
Facilitates booking and reservation management for guests and hosts. Users can check availability, book properties for specific dates, and receive confirmation, while hosts can track upcoming reservations.
### 4. Reviews & Ratings
Allows guests to leave reviews and rate properties they have stayed in. This feature helps maintain transparency, builds trust among users, and assists hosts in improving their services.
### 5. Payments & Transactions
Manages secure payment processing for bookings. Users can pay for reservations online, and the system tracks payment status, ensuring safe and reliable financial transactions.
