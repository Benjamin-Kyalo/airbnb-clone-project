# airbnb-clone-project
 airbnb-clone-project

# Overview  
A minimalist clone of AirBnB’s back-end, built for learning REST APIs and data modeling.

# Goals  
- Practice building a RESTful API with Python  
- Design a clear data model for users, listings, bookings  
- Implement CRUD operations and relationships  

# Tech Stack  
- Language: Python 
- Framework: Flask or Django REST Framework  
- Database: MySQL or PostgreSQL  
- Version Control: Git & GitHub  


# Team Roles
1. Backend Developer
- Writes its algorithms and business logic.
- Devises the overall app architecture.
- Writes its algorithms and business logic.

2. Database Administrator (DBA)
- Models the data schema, manages migrations, optimizes queries, and ensures data integrity.

3. Business analyst (BA)
- Understands customer’s business processes
- Translates customer business needs into requirements

4. Product owner (PO)
- Holds responsibility for a product vision and evolution
- Makes sure the final product meets customer requirements

5. Project manager (PM)
- Makes sure a product or its part is delivered on time and within budget
- Manages and motivates the software development team

6. UI/UX designer
- Transforms a product vision into user-friendly designs
- Creates user journeys for the best user experience and highest conversion rates

7. Software architect
- Designs a high-level software architecture
- Selects appropriate tools and platforms to implement the product vision
- Sets up code quality standards and performs code reviews

8. Software developer
- Engineers and stabilizes the product
- Solves any technical problems emerging during the development lifecycle

9. Quality assurance (QA) engineer
- Makes sure an application performs according to requirements
- Spots functional and non-functional defects

10. Test automation engineer
- Designs a test automation ecosystem
- Writes and maintains test scripts for automated testing
  
11. DevOps engineer
- Facilitates cooperation between development and operations teams
- Builds continuous integration and continuous delivery (CI/CD) pipelines for faster delivery

# Technology Stack
- Django: A high-level Python web framework used for building the RESTful API.
- Django REST Framework: Provides tools for creating and managing RESTful APIs.
- PostgreSQL: A powerful relational database used for data storage.
- GraphQL: Allows for flexible and efficient querying of data.
- Celery: For handling asynchronous tasks such as sending notifications or processing payments.
- Redis: Used for caching and session management.
- Docker: Containerization tool for consistent development and deployment environments.
- CI/CD Pipelines: Automated pipelines for testing and deploying code changes.

# Database Design
Entities & Key Fields

User

id (PK), email, hashed_password, first_name, last_name

Property

id (PK), owner_id (FK → User), title, address, price_per_night

Booking

id (PK), user_id (FK → User), property_id (FK → Property), start_date, end_date

Review

id (PK), booking_id (FK → Booking), rating, comment, created_at

Payment

id (PK), booking_id (FK → Booking), amount, payment_method, status

# Feature Breakdown
- User Management

Sign up, log in/out, and profile updates (password reset, email).

- Property Management
  
CRUD on listings: create new properties, edit details, delete listings.

- Booking System
  
Search availability, book a stay, view/cancel bookings.

- Reviews & Ratings
  
After checkout, users can leave a rating and text review.

- Payments
  
Securely process payments (e.g., via Stripe) and track transaction status.

# API Security
Authentication
JSON Web Tokens (JWT) to verify user identity on every request.

- Authorization
  
Role-based access: only owners can modify their own listings; only bookers can cancel their bookings.

- Rate Limiting
  
Throttle endpoints to prevent abuse (e.g., max 100 requests/hour).

- Data Protection

HTTPS everywhere, hashed passwords (bcrypt/Argon2), input validation to avoid injections.







