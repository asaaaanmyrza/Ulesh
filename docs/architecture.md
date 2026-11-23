# Ulesh System Architecture

## 1. Overview

Ulesh is a proposed digital platform designed to connect restaurants, grocery stores, and charitable organizations to facilitate food donations and reduce food waste.

The platform allows food donors to publish available surplus food, while verified charitable organizations can browse listings and submit donation requests.

The planned system follows a modular architecture that separates the frontend, backend, and data storage. This structure is intended to make the platform easier to maintain, extend, and adapt to different technical environments.

## 2. Technology Stack

The initial development of Ulesh is planned around the following technologies:

| Component | Technology | Purpose |
|---|---|---|
| Frontend | Vue.js | User interface and client-side interactions |
| Backend | FastAPI | API endpoints and application logic |
| Database | SQLite | Initial data storage and support for the basic application workflow |

### 2.1. Database Scalability

SQLite is selected for the initial development stage to support the basic application workflow with a lightweight database solution.

As the platform develops and its data and user requirements grow, PostgreSQL may be considered as a future database solution to support increased scalability and more advanced database operations.

The potential migration is a future consideration rather than an implemented feature.

## 3. Main System Components

### 3.1. Frontend (Vue.js)

The frontend provides the user interface through which participants interact with Ulesh.

The platform supports two main user categories:

- **Food Donors:** Restaurants and grocery stores that publish surplus food offers and manage donation requests.
- **Charitable Organizations:** Verified organizations that browse available food offers and submit donation requests.

The frontend is responsible for displaying food listings, collecting user input, and communicating with the backend through API requests.

### 3.2. Backend (FastAPI)

The backend handles the main application logic and processes requests received from the frontend.

Its planned responsibilities include:

- User registration and account management.
- Manual verification of restaurants and charitable organizations.
- Creating, updating, and managing food offers.
- Submitting, reviewing, and managing donation requests.
- Updating request statuses.
- Enforcing access permissions based on user roles.

### 3.3. Database (SQLite)

The database stores the information required for the platform's basic operations.

The planned data includes:

- User accounts and organization information.
- Verification statuses.
- Food offers, quantities, and expiration dates.
- Storage conditions and allergen information.
- Donation requests and their statuses.

SQLite is intended for the initial development stage. PostgreSQL may be considered as the platform grows.

### 3.4. Notification Service

A notification component may be introduced to inform users about important events, including:

- New donation requests.
- Request approvals or rejections.
- Changes in food offer availability.
- Upcoming collection deadlines.

This component is considered a planned extension of the system.

## 4. System Workflow and Data Flow

The planned interaction between the main components follows this sequence:

1. A restaurant or grocery store registers on the platform.
2. The organization undergoes manual verification before it can publish food offers.
3. A verified food donor publishes an offer containing food details, quantity, expiration information, storage conditions, allergen information, and collection details.
4. The backend validates and processes the submitted information.
5. The offer is stored in the database and becomes available to verified charitable organizations.
6. A verified charitable organization browses available offers and submits a donation request.
7. The food donor reviews the request and approves or rejects it.
8. The request status is updated and communicated to the relevant participants.
9. After approval, both parties coordinate the food collection and transfer.

## 5. Safety and Do No Harm

Food donation involves potential health and safety risks. Therefore, Ulesh is designed around the following principles:

### 5.1. Food Safety First

Food donors must only publish products that are safe for consumption, correctly stored, and within their expiration or best-before dates.

Responsibility for food quality remains with the donating business. Food listings must include relevant handling, storage, and allergen information.

### 5.2. Verified Participants

Restaurants, grocery stores, and charitable organizations must undergo manual verification before they can publish or claim food donations.

This requirement is intended to reduce misuse of the platform and encourage responsible participation.

### 5.3. Non-Discrimination

All verified charitable organizations should have equal access to available food listings, regardless of their size, location, or the beneficiaries they serve.

Ulesh does not permit discriminatory content or behavior on the platform.

### 5.4. Respectful Community

All platform participants and contributors are expected to follow the project's Code of Conduct and maintain respectful communication.

## 6. Platform Independence

Ulesh is intended to avoid dependence on a single proprietary platform or service.

The proposed architecture supports platform independence through the following principles:

- **Open Technologies:** The planned stack uses widely available technologies, including Vue.js, FastAPI, and SQLite.
- **Modular Architecture:** The frontend, backend, and data storage are separated, allowing individual components to be modified or replaced.
- **Portable Data Storage:** The system is designed to avoid unnecessary dependence on a single database provider.
- **Replaceable Components:** External services and integrations should be replaceable without requiring a complete redesign of the platform.
- **Open Standards:** Common communication protocols and data formats are intended to support interoperability.

These principles are intended to reduce vendor lock-in and make future deployment in different environments possible.

## 7. Deployment Strategy

The planned deployment process separates the frontend, backend, and database components.

The Vue.js frontend will provide the user-facing application, while the FastAPI backend will handle application logic and API communication. SQLite will initially store the application's data.

Future deployment may involve hosting the frontend and backend independently and using a more scalable database solution if required.

Specific hosting providers and deployment infrastructure have not yet been finalized.

## 8. Future Development

The proposed architecture provides a foundation for the future development of Ulesh.

Potential improvements include:

- Migrating from SQLite to PostgreSQL if scalability requirements increase.
- Introducing a dedicated notification system.
- Improving organization verification and account management.
- Expanding food safety validation and monitoring.
- Improving system performance and supporting a growing number of users.

These improvements represent possible future development directions and should not be interpreted as currently implemented functionality.

## 9. Architecture Summary

Ulesh follows a planned modular architecture based on Vue.js, FastAPI, and SQLite for its initial development stage.

The system separates user interaction, application logic, and data management while supporting different user roles, manual organization verification, and food safety principles.

Its modular structure and use of widely available technologies are intended to support maintainability, future scalability, and independence from proprietary platforms.
