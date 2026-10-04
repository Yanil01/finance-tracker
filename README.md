# Finance Tracker

A modern full-stack personal finance management application built with Angular, Spring Boot, and PostgreSQL.

The application enables users to manage accounts, record income and expenses, create budgets, track savings goals, and analyze their financial activity through dashboards and reports.

---

## Features

### Authentication

- User registration
- User login
- Logout
- Protected routes
- User-specific financial data

### Account Management

- Create account
- Update account
- Delete account
- View account balance
- Support multiple account types

Examples:

- Cash
- Bank Account
- Wallet
- Credit Card

### Transaction Management

- Add income
- Add expenses
- Edit transactions
- Delete transactions
- Categorize transactions
- Filter transactions
- Track account balances

### Category Management

Users can organize transactions into categories such as:

**Income**

- Salary
- Freelance
- Investment
- Business

**Expenses**

- Food
- Transportation
- Rent
- Shopping
- Utilities
- Entertainment

### Dashboard

The dashboard provides an overview of:

- Total balance
- Monthly income
- Monthly expenses
- Monthly savings
- Recent transactions
- Spending by category
- Income vs expense analysis

### Budget Management

Users can:

- Create category-based budgets
- Define spending limits
- Track budget usage
- View remaining budget
- Receive budget alerts

### Savings Goals

Users can:

- Create savings goals
- Define target amounts
- Add contributions
- Track progress
- Set target dates

### Financial Reports

The application provides:

- Monthly reports
- Income summaries
- Expense summaries
- Category breakdowns
- Savings analysis

---

## Technology Stack

### Frontend

- Angular
- TypeScript
- Angular Router
- Reactive Forms
- HttpClient
- Tailwind CSS
- SCSS

### Backend

- Java
- Spring Boot
- Spring Web
- Spring Data JPA
- Spring Boot DevTools
- Spring Security
- Bean Validation
- Maven

### Database

- PostgreSQL

### Development Tools

- Git
- GitHub
- PlantUML
- Postman
- IntelliJ IDEA
- DataGrip
- PostgreSQL JDBC Driver

---

## System Architecture

```text
Angular Client
      |
      | HTTP / JSON
      | REST API
      v
Spring Boot
      |
      v
Controller
      |
      v
Service
      |
      v
Repository
      |
      v
JPA / Hibernate
      |
      v
PostgreSQL
```

---

## Project Structure

```text
finance-tracker/
│
├── client/
│   └── Angular frontend
│
├── server/
│   └── Spring Boot backend
│
├── .env.example
├── .gitignore
└── README.md
```

### Client Structure

```text
client/src/app/

├── core/
│   ├── guards/
│   ├── interceptors/
│   ├── models/
│   └── services/
│
├── features/
│   ├── auth/
│   ├── dashboard/
│   ├── accounts/
│   ├── categories/
│   ├── transactions/
│   ├── budgets/
│   ├── goals/
│   ├── reports/
│   └── profile/
│
├── layouts/
│
└── shared/
    └── components/
```

### Server Structure

```text
server/src/main/java/com/yanil/financetracker/

├── config/
├── controller/
├── dto/
│   ├── request/
│   └── response/
├── entity/
├── enums/
├── exception/
├── mapper/
├── repository/
├── security/
├── service/
└── FinanceTrackerApplication.java
```

---

## Domain Model

The main domain objects are:

```text
User
 |
 ├── Account
 |      |
 |      └── Transaction
 |
 ├── Category
 |      |
 |      ├── Transaction
 |      └── Budget
 |
 ├── Budget
 |
 ├── SavingsGoal
 |
 └── Notification
```

---

## Prerequisites

Before running the application, install:

- Java
- Maven, or use the included Maven Wrapper
- Node.js
- npm
- PostgreSQL
- Git

---

## Getting Started

### 1. Clone the Repository

```bash
git clone <repository-url>
cd finance-tracker
```

---

## Frontend Setup

Move into the Angular project:

```bash
cd client
```

Install dependencies:

```bash
npm install
```

Start the Angular development server:

```bash
npm start
```

The Angular development server will print the local URL in the terminal.

---

## Backend Setup

Open another terminal and move to:

```bash
cd server
```

Run Spring Boot using the Maven Wrapper:

```bash
./mvnw spring-boot:run
```

---

## Database Setup

Create a PostgreSQL database:

```sql
CREATE DATABASE finance_tracker;
```

Configure the required environment variables:

```bash
export DB_USERNAME=your_username
export DB_PASSWORD=your_password
```

The Spring Boot datasource configuration reads these environment variables.

Example:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/finance_tracker

spring.datasource.username=${DB_USERNAME}
spring.datasource.password=${DB_PASSWORD}
```

---

## API Structure

The REST API is organized around the following resources:

```text
/api/auth
/api/accounts
/api/categories
/api/transactions
/api/dashboard
/api/budgets
/api/goals
/api/reports
/api/users
/api/notifications
```

---

## Development Roadmap

### Phase 1

- [ ] Project setup
- [ ] PostgreSQL configuration
- [ ] Angular/Spring Boot connectivity

### Phase 2

- [ ] User registration
- [ ] Authentication
- [ ] Route protection

### Phase 3

- [ ] Account management

### Phase 4

- [ ] Category management

### Phase 5

- [ ] Income management
- [ ] Expense management
- [ ] Transaction filtering

### Phase 6

- [ ] Financial dashboard
- [ ] Dashboard charts

### Phase 7

- [ ] Budget management
- [ ] Budget progress tracking

### Phase 8

- [ ] Savings goals
- [ ] Goal contributions

### Phase 9

- [ ] Monthly financial reports
- [ ] Category reports

### Phase 10

- [ ] Notifications
- [ ] Recurring transactions

### Phase 11

- [ ] Automated testing
- [ ] Security review
- [ ] Production deployment

---

## Development Methodology

The application follows vertical feature development.

Each feature is implemented through:

```text
Database
   ↓
Entity
   ↓
Repository
   ↓
Service
   ↓
Controller
   ↓
REST API
   ↓
Angular Service
   ↓
Angular Component
   ↓
User Interface
   ↓
Testing
```

A new feature should not be considered complete until its full frontend-to-database flow has been implemented and tested.

---

## Object-Oriented Design

The application applies object-oriented concepts including:

- Encapsulation
- Abstraction
- Polymorphism
- Composition
- Separation of concerns

The system is modeled using UML diagrams including:

- Use Case Diagram
- Class Diagram
- Domain Model
- Activity Diagram
- Sequence Diagram
- State Diagram
- Package Diagram
- Component Diagram
- Deployment Diagram
- Entity Relationship Diagram

---

## Security

The application is designed so that:

- Passwords are never stored as plain text.
- Protected APIs require authentication.
- Users can access only their own financial resources.
- Sensitive configuration is provided outside source control.
- Backend validation is applied to incoming requests.

---

## Author

**Yanil Gurmachhan Magar**

---

## Project Status

Under active development.