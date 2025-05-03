## Project Goals

- **User Management**: Implement a secure system for user registration, authentication, and profile management.
- **Property Management**: Develop features for property listing creation, updates, and retrieval.
- **Booking System**: Create a booking mechanism for users to reserve properties and manage booking details.
- **Payment Processing**: Integrate a payment system to handle transactions and record payment details.
- **Review System**: Allow users to leave reviews and ratings for properties.
- **Data Optimization**: Ensure efficient data retrieval and storage through database optimizations.

## Technology Stack

- **Django**: A high-level Python web framework used for building the RESTful API.
- **Django REST Framework**: Provides tools for creating and managing RESTful APIs.
- **PostgreSQL**: A powerful relational database used for data storage.
- **GraphQL**: Allows for flexible and efficient querying of data.
- **Celery**: For handling asynchronous tasks such as sending notifications or processing payments.
- **Redis**: Used for caching and session management.
- **Docker**: Containerization tool for consistent development and deployment environments.
- **CI/CD** Pipelines: Automated pipelines for testing and deploying code changes.

## Team Roles

- **Business Analyst (BA)**: They translate an abstract product idea into a set of tangible requirements.
- **Product Owner (PO)**: A decision-maker. Balancing both business needs and market trends, they define a business strategy, shape up the product vision, make sure it satisfies customer needs, and manage a product backlog.
- **Project Manager (PM)**: Responsible for distributing tasks across team members, planning work activities, and updating project status.
- **UI/UX designer**: Throughout the development lifecycle, helps achieve business goals via functional and engaging user experiences, as well as analyzing, evaluating, and enhancing those experiences over time.
- **Software architect**: Decides which services and databases should communicate together, how integrations should work, and how to ensure that the product is secure and stable.
- **Frontend developer**: Creates the part of an application that users interact with, ensuring that an app offers an equally smooth experience to all—no matter the device, platform, or operational system.
- **Backend Developer**: Responsible for implementing API endpoints, database schemas, and business logic.
- **Database Administrator**: Manages database design, indexing, and optimizations.
- **DevOps Engineer**: Handles deployment, monitoring, and scaling of the backend services.
- **QA Engineer**: Ensures the backend functionalities are thoroughly tested and meet quality standards.

## Database Design
- **Users** Relationships: Can list and view proterties, make a booking and ratings
    - id
    - name
    - email
- **Properties**: Relationships: Are added and viewed by Users and booked afterwards
    - id
    - location
    - rooms
    - name
- **Bookings** Relationships: Bookings are made on ptoperties
     - id
     - date
     - booked
- **Reviews**. Relationships: Are made by Users(customers) on properties
    - title
    - text
    - rating
    - date
- **Payments**. Relationships: Made by users when they book a particular property
    - date
    - amount
    - success

## Feature Breakdown
- **User management** This will contain different users such as customers, Hotel managers and administrators. 
- **property management**: Will make it possible to insert new properties and provide further descriptions.
- **Booking System**: This will enable potential customers to book their prefered properties of interest.
- **payment Integration**: The customer will pay for the room through the payment system.

## API Security
- **Authentication**: This feature will verify a user
- **Authorization**: This will give permission to the user to perform actions when verification is completed.
- **Rate limiting**: Feature to control the amount of ratings a verified user can do

## CI/CD Pipeline
*For laughs 😂: CI/CD Pipeline is like connecting PVC pipe to spray something*
CI/CD is Continuous Integration and Continuous Deployment/Delivery. A series of steps that devs must follow to deliver 
a new version of a software. CI/CD pipelines are a practice to improve software delivery throughout the software delivery 
lifecycle through automation.
- **GitHub Actions**: GitHub Actions allows developers to create workflows that run when certain events happen in a repository, 
such as a pull request or a push to a branch. These workflows can then execute various tasks, including running tests, building applications,
 and deploying to different environments. 
- **Docker**: Allows devs to package applications with all the dependencies into a standardiaed unit for software development.
It provides uniformity and the assurance that the application runs the same way in different environments from development to production.