
<p align="center">
  <img src="https://github.com/NouhanDoumbouya/airbnb-clone-project/blob/main/images/AIRBNB.jpeg" alt="Airbnb Image" width="400" style="border-radius: 30px;"/>
</p>

# 🏡 Airbnb Clone Backend Project

> A real-world backend clone of Airbnb designed to simulate a robust booking platform using Django, PostgreSQL, GraphQL, and more.

---

## 📖 About the Project

The **Airbnb Clone Project** is a comprehensive, real-world application designed to simulate the development of a robust booking platform like Airbnb. It involves a deep dive into full-stack development, focusing on backend systems, database design, API development, and application security.

This project enables learners to understand complex architectures, workflows, and collaborative team dynamics while building a scalable web application.

---

## 🎯 Learning Objectives

By completing this project, learners will:

- ✅ Master collaborative team workflows using GitHub.
- 🧠 Deepen understanding of backend architecture and database design.
- 🔒 Implement advanced security measures for APIs.
- 🚀 Gain proficiency in CI/CD pipeline design and deployment.
- 📚 Strengthen technical documentation and planning skills.
- ⚙️ Integrate Django, MySQL/PostgreSQL, and GraphQL in a unified ecosystem.

---

## 🧪 Task List

- [0. Project Requirements](#-requirements)
- [1. Team Roles](#-team-roles)
- [2. Technology Stack Overview](#-technology-stack)
- [3. Database Design Overview](#-database-design)
- [4. Feature Breakdown](#-feature-breakdown)
- [5. API Security Overview](#-api-security)
- [6. CI/CD Pipeline Overview](#-cicd-pipeline)

---

## ✅ Requirements

To complete the tasks, you must:

- Have a GitHub account.
- Understand Markdown syntax.
- Be experienced with Django and MySQL/PostgreSQL.
- Be familiar with software lifecycle, CI/CD, and security best practices.
- Know tools like Docker and GitHub Actions.
- Understanding of the technology stacks
---

## 👥 Team Roles

| Role                 | Responsibilities                                                                 |
|----------------------|----------------------------------------------------------------------------------|
| 🧑‍💻 Backend Developer  | Build APIs, manage logic, implement features like auth, booking, and listings.     |
| 🧠 Database Admin     | Design schema, write migration scripts, manage relationships and performance.    |
| 🔐 Security Engineer  | Implement API auth, data validation, and user input sanitization.                |
| ⚙️ DevOps Engineer    | Set up Docker, CI/CD, environment variables, and manage deployment pipelines.    |
| 🧪 QA Engineer        | Write unit/integration tests and ensure code meets quality standards.            |

---

## 💻 Technology Stack

| Technology       | Purpose                                                                 |
|------------------|-------------------------------------------------------------------------|
| **Django** [![Django](https://github.com/NouhanDoumbouya/airbnb-clone-project/blob/main/images/django.png)](https://docs.djangoproject.com/)| Core backend web framework for handling models, views, and APIs         |
| **Django REST** [![DjangoRestFramework](https://github.com/NouhanDoumbouya/airbnb-clone-project/blob/main/images/drf-logo2.png)](https://www.django-rest-framework.org/) | Used to expose RESTful endpoints for frontend consumption               |
| **GraphQL** [![GraphQL](https://github.com/NouhanDoumbouya/airbnb-clone-project/blob/main/images/graphql.png)](https://graphql.org/)     | Offers efficient querying of complex data relationships                 |
| **PostgreSQL** [![PostgreSQL](https://github.com/NouhanDoumbouya/airbnb-clone-project/blob/main/images/Postgresql_elephant.svg.png)](https://www.postgresql.org/)  | Relational database for managing structured data                        |
| **Docker** [![Docker](https://github.com/NouhanDoumbouya/airbnb-clone-project/blob/main/images/docker.jpg)](https://www.docker.com/)      | Containerization for consistent environments                            |
| **Celery + Redis** [![Celery+Redis](https://github.com/NouhanDoumbouya/airbnb-clone-project/blob/main/images/redis_celery.jpg)](https://docs.celeryq.dev/en/3.1/getting-started/brokers/redis.html) | Background tasks (email sending, notifications) and caching            |
| **GitHub Actions** [![GithubActions](https://github.com/NouhanDoumbouya/airbnb-clone-project/blob/main/images/github_actions.jpeg)](https://github.com/features/actions) | CI/CD pipeline automation                                              |

---

## 🗃️ Database Design

| Entity       | Fields Example | Relationships                                            |
|--------------|----------------|-----------------------------------------------------------|
| **User**     | id, name, email, password, is_host         | One user can own many properties and make many bookings   |
| **Property** | id, title, description, location, owner_id | Belongs to a user (owner), has many bookings and reviews |
| **Booking**  | id, user_id, property_id, checkin, checkout| Belongs to a user and a property                          |
| **Review**   | id, user_id, property_id, rating, comment  | Belongs to a user and a property                          |
| **Payment**  | id, booking_id, amount, status, timestamp  | Tied to a specific booking                               |

Relationships:
- A **User** can create many **Properties**.
- A **User** can make many **Bookings**.
- A **Property** can have many **Bookings** and **Reviews**.
- A **Booking** has one **Payment**.

---

## 🧩 Feature Breakdown

### 👥 User Management
- Allows users to sign up, log in, update profiles, and become hosts.
- Provides authentication and authorization mechanisms using JWT.

### 🏠 Property Management
- Hosts can list, edit, and remove rental properties.
- Each property includes description, price, photos, location, and availability.

### 📆 Booking System
- Users can book properties for a date range.
- Handles availability, booking history, and conflicts.

### 💳 Payment Processing
- Secure handling of transactions for bookings.
- Integrates with payment providers like Stripe/PayPal.

### ⭐ Review System
- Users can leave ratings and feedback on properties after a stay.
- Reviews improve property visibility and host credibility.

---

## 🔒 API Security

Security is critical in handling sensitive data and preventing abuse.

- **Authentication**: JWT-based auth for secure session handling.
- **Authorization**: Role-based access to routes (e.g., host-only actions).
- **Rate Limiting**: Prevents abuse and brute-force attacks.
- **Input Validation**: Prevents SQL injection, XSS, and other attacks.
- **HTTPS**: Encrypts communication between client and server.
- **CSRF/XSRF Protection**: Prevents cross-site request forgery for state-changing actions.

Each of these measures ensures that user data, payments, and application integrity remain protected.

---

## 🔄 CI/CD Pipeline

**CI/CD (Continuous Integration & Continuous Deployment)** automates code testing, building, and deployment.

- **Why it matters**: Reduces manual work, speeds up feedback loops, and ensures code reliability.
- **What it does**:
  - Runs tests automatically on pull requests.
  - Deploys to staging or production after successful builds.
- **Tools used**:
  - **GitHub Actions**: Automates workflow for build, test, and deploy.
  - **Docker**: Containerizes application for consistent deployment.
  - **Heroku / AWS / DigitalOcean**: (Optional) Hosts the deployed application.

---

## 📬 Contributing

1. Fork the repository  
2. Clone your fork:  
   ```bash
   git clone https://github.com/your-username/airbnb-clone-project.git
