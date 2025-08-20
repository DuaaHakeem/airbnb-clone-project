# airbnb-clone-project

## Overview
This project is a full-stack web application, developed as a clone of Airbnb using Django, MySQL, and GraphQL. It replicates the core functionality of Airbnb by allowing users to create accounts, browse property listings, check availability, and make bookings. The project also includes secure API development, database design for managing users, listings, and reservations, as well as CI/CD pipeline integration with Docker and GitHub Actions to simulate a real-world deployment workflow.





## Project Goals  
- **User Management**: Implement a secure system for user registration, authentication, and profile management.  
- **Property Management**: Develop features for property listing creation, updates, and retrieval.  
- **Booking System**: Create a booking mechanism for users to reserve properties and manage booking details.  
- **Payment Processing**: Integrate a payment system to handle transactions and record payment details.  
- **Review System**: Allow users to leave reviews and ratings for properties.  
- **Data Optimization**: Ensure efficient data retrieval and storage through database optimizations.  
  



  ## Technology Stack  
- **Django**: A high-level Python web framework used for building the RESTful API.  
- **Django REST Framework (DRF)**: Provides tools for creating and managing RESTful APIs.  
- **PostgreSQL**: A powerful relational database used for data storage.  
- **GraphQL**: Enables flexible and efficient querying of data.  
- **Celery**: Handles asynchronous tasks such as sending notifications or processing payments.  
- **Redis**: Used for caching and session management.  
- **Docker**: Containerization tool for consistent development and deployment environments.  
- **CI/CD Pipelines**: Automated pipelines for testing and deploying code changes.


## 👥 Team Roles

- **Backend Developer**: Implement the core of an app, its algorithms and business logic and perform the tasks of an architec.
- **Database Administrator**: Manages database design, indexing, and optimizations. 
- **DevOps Engineer**: Facilitates cooperation between development and operations teams and builds continuous integration and continuous delivery (CI/CD) pipelines for faster delivery.
- **QA Engineer**: Makes sure an application performs according to requirements and spots functional and non-functional defects.

  
 ## Database Design

 ### Key Entities  

1. **Users**  
   - Fields: `user_id`, `name`, `email`, `password_hash`, `role`  
   - Relationships: A user can list multiple properties, make multiple bookings, and leave reviews.  

2. **Properties**  
   - Fields: `property_id`, `owner_id (FK to Users)`, `title`, `description`, `location`, `price_per_night`  
   - Relationships: A property belongs to a user (owner) and can have multiple bookings and reviews.  

3. **Bookings**  
   - Fields: `booking_id`, `user_id (FK to Users)`, `property_id (FK to Properties)`, `start_date`, `end_date`, `status`  
   - Relationships: A booking belongs to a user and a property.  

4. **Payments**  
   - Fields: `payment_id`, `booking_id (FK to Bookings)`, `amount`, `payment_method`, `payment_status`  
   - Relationships: A payment is linked to a booking.  

5. **Reviews**  
   - Fields: `review_id`, `user_id (FK to Users)`, `property_id (FK to Properties)`, `rating`, `comment`  
   - Relationships: A review belongs to a user and a property.


  ## Feature Breakdown

  1. **User Management**

This feature enables secure registration, login, and profile management for users. It ensures that both hosts and guests have authenticated access to the platform, maintaining data security and personalized experiences.

2. **Property Management**

Hosts can create, update, and manage property listings through this feature. It allows detailed descriptions, pricing, and availability to be stored, making it easy for guests to browse and select accommodations.

3. **Booking System**

The booking feature enables users to reserve properties and manage their reservations. It handles check-in and check-out details, ensuring a smooth and reliable process for both guests and hosts.

4. **Payment Processing**

This feature allows users to make secure payments for their bookings. It integrates transaction handling, ensuring accurate record-keeping of payment details and enhancing trust on the platform.

5. **Review System**

Users can leave ratings and reviews for properties they have stayed in. This contributes to transparency and helps future guests make informed decisions while also providing feedback to hosts.

6. **Database Optimization**

Indexes and caching strategies are implemented to improve the speed and efficiency of data retrieval. This ensures the platform can scale effectively while maintaining fast response times.
     
