# Local Setup & Development Guide

This guide will walk you through setting up your local environment for development, running tests, and preparing code for production.

---

## 🛠️ Prerequisites

Ensure you have the following installed on your system before proceeding:

- **Node.js**: Version `18.x` or higher
- **Docker & Docker Compose**: For local databases and dependency containers
- **Package Manager**: `npm` (packaged with Node.js) or `pnpm`/`yarn`
- **Git**

---

## 🚀 Setup Steps

### 1. Clone the Repository
```bash
git clone https://github.com/username/repo-name.git
cd repo-name
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Setup Environment Variables
Create a local `.env` file copying the keys from the example template:
```bash
cp .env.example .env
```
Open `.env` and fill out any secret credentials (API keys, DB passwords).

### 4. Start Local Services (Docker)
If the project relies on external databases or services, start them up using Docker:
```bash
docker-compose up -d
```
This typically provisions:
- PostgreSQL database
- Redis cache/broker

### 5. Run Database Migrations
Make sure the local database schemas are updated:
```bash
npm run db:migrate
```

### 6. Start the Development Server
Run the local dev compiler:
```bash
npm run dev
```
The application should now be accessible at `http://localhost:3000`.

---

## 🧪 Testing

We use [Jest / Vitest / Playwright] for test execution.

### Run Unit Tests
```bash
npm run test
```

### Run Tests with Coverage Report
```bash
npm run test:coverage
```

---

## 🎨 Quality & Formatting

We enforce standard formatting and linting rules to maintain clean code.

```bash
# Run Linter
npm run lint

# Run Auto-Formatter
npm run format
```
Ensure all lint errors are resolved before opening a Pull Request.
