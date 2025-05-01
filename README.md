# 🏡 StayEase - Airbnb Clone Project

<p align="center">
  <img src="https://github.com/NouhanDoumbouya/airbnb-clone-project/blob/main/images/AIRBNB.jpeg" alt="Airbnb Image" width="400" style="border-radius: 30px;"/>
</p>

Welcome to **StayEase**, a full-stack clone of the Airbnb platform. This project demonstrates a modern booking system with features like property listings, detailed pages, user authentication, and secure checkout, all built using a scalable frontend and backend architecture.

---

## 📚 Table of Contents

- [🎯 Project Overview](#project-overview)
- [🖥️ Frontend Overview](#frontend-overview)
  - [Technologies (Frontend)](#technologies-frontend)
  - [UI/UX Design Planning](#uiux-design-planning)
  - [Figma Design Specifications](#figma-design-specifications)
  - [Primary Pages](#primary-pages)
  - [UI Components](#ui-components)
- [🗄️ Backend Overview](#backend-overview)
  - [Technologies (Backend)](#technologies-backend)
  - [API Endpoints](#api-endpoints)
  - [Database Models](#database-models)
  - [Authentication](#authentication)
- [🚀 Deployment Strategy](#deployment-strategy)
- [🧪 Testing Strategy](#testing-strategy)
- [👥 Project Roles and Responsibilities](#project-roles-and-responsibilities)
- [📅 FRONTEND Timeline](#frontend-timeline)
- [📝 Contributing](#contributing)
- [📎 Resources](#resources)

---

##  Project Overview

**StayEase** is a feature-rich accommodation booking platform, aiming to deliver:

- Intuitive search and filter system for users
- Fully responsive UI/UX inspired by Airbnb
- Real-time booking process with secure payment
- Scalable architecture and modular component design

---

##  Frontend Overview

### Technologies (Frontend)

- **React.js** with **Next.js** for Server-Side Rendering and Routing
- **TypeScript** for scalable type-safe code
- **TailwindCSS** for utility-first CSS
- **Figma** for design prototyping and layout planning
- **Redux Toolkit / Context API** for state management

---

### UI/UX Design Planning

#### Design Goals

- Create an intuitive booking experience
- Maintain visual consistency and fast-loading UI
- Prioritize mobile responsiveness and accessibility

#### Key Features

- Search and filter properties by criteria
- View property details including gallery and reviews
- Streamlined booking with confirmation
- Secure user authentication and session management

---

### Figma Design Specifications

#### 🎨 Color Palette

| Style | Hex Code |
|-------|----------|
| Primary | `#FF5A5F` |
| Secondary | `#008489` |
| Background | `#FFFFFF` |
| Text | `#222222` |
| Secondary Text | `#717171` |

#### ✍️ Typography

- **Primary Font**: Circular
- **Headings**: Bold (700), 24px – 32px
- **Body Text**: Medium (500), 16px
- **Secondary**: Book (400), 14px

#### Importance of Design Consistency

Recognizing design specifications from Figma ensures accurate implementation of layout, colors, and typography. This consistency elevates usability, professionalism, and brand trust.

---

### Primary Pages

| Page | Description |
|------|-------------|
| **Property Listing View** | Grid display of properties with filters |
| **Listing Detailed View** | Gallery, description, amenities, booking form |
| **Simple Checkout View** | Summary and payment form for finalizing booking |

---

### UI Components

| Component | Description |
|-----------|-------------|
| **Navbar** | Logo, search bar, user navigation |
| **Property Card** | Image, location, price, rating, favorite icon |
| **Footer** | Site navigation, social links, copyright |
| **Form Components** | Input fields, dropdowns, date picker |

All components are modular, reusable, and mobile-responsive.

---

##  Backend Overview

### Technologies (Backend)

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

### API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/listings/` | GET | Retrieve all property listings |
| `/api/listings/<id>/` | GET | Retrieve property by ID |
| `/api/bookings/` | POST | Create new booking |
| `/api/auth/register/` | POST | User registration |
| `/api/auth/login/` | POST | Login and receive token |
| `/api/user/bookings/` | GET | Authenticated user bookings |

---

### Database Models

- **User**: Custom user model (email login)
- **Listing**: Title, location, price, description, host
- **Booking**: Start/end date, user, property, guests
- **Review**: Rating, comments, linked to listings

---

### Authentication

- **JWT Tokens** for secure, stateless session handling
- Middleware to protect sensitive routes
- Password hashing and user verification workflows

---

## 🚀 Deployment Strategy

| Tool | Purpose |
|------|---------|
| **Vercel** | Host the frontend |
| **Heroku / Render** | Deploy Django backend |
| **Docker** | Containerize services for local/dev |
| **GitHub Actions** | CI/CD workflow automation |

---

## 🧪 Testing Strategy

| Test Type | Tool |
|-----------|------|
| Unit Testing | Jest (Frontend), Pytest (Backend) |
| Integration Testing | React Testing Library |
| E2E Testing | Cypress |
| Manual QA | GitHub Projects Board for bugs |

---

##  Project Roles and Responsibilities

| Role | Responsibilities |
|------|------------------|
| **Project Manager** | Oversees deadlines, team sync, and priorities |
| **Frontend Developers** | Build UI components, integrate APIs |
| **Backend Developers** | Design database, build REST & GraphQL APIs |
| **Designers** | Design UI, ensure accessibility and UX |
| **QA Engineers** | Write and run tests, track issues |
| **DevOps Engineers** | Manage deployment pipelines and cloud setup |
| **Product Owner** | Define features, prioritize tasks |
| **Scrum Master** | Run agile ceremonies and remove blockers |

---

##  FRONTEND Timeline

| Date | Milestone |
|------|-----------|
| **Apr 28** | GitHub Repo Initialization & UI Planning |
| **Apr 29 – 30** | Build Main Pages (Home, Listings, Detail) |
| **May 1 – 2** | Backend API integration & Checkout logic |
| **May 3 – 4** | Responsive design finalization & Testing |
| **May 5** | Final QA + Deployment + Presentation Prep |

---

##  Contributing

We welcome contributions! Here's how:

1. Fork this repository  
2. Create your branch: `git checkout -b feature/your-feature`  
3. Commit your changes: `git commit -m 'Add your feature'`  
4. Push to the branch: `git push origin feature/your-feature`  
5. Submit a Pull Request  

---

##  Resources

- [React Docs](https://reactjs.org/)
- [Next.js Docs](https://nextjs.org/)
- [TailwindCSS Docs](https://tailwindcss.com/)
- [Django REST Framework](https://www.django-rest-framework.org/)
- [Graphene for Django](https://docs.graphene-python.org/)
- [PostgreSQL Docs](https://www.postgresql.org/docs/)
- [Figma](https://www.figma.com/)
- [JWT Auth](https://jwt.io/)
- [Airbnb Official](https://www.airbnb.com/)

---

<p align="center"><strong>Crafted by NOUHAN DOUMBOUYA ✨ | 2025</strong></p>
