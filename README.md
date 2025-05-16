# 🚀 AI-Powered Campaign CRM – Backend

Welcome to the **backend service** of an advanced, intelligent campaign management platform. This secure, scalable API infrastructure powers user management, campaign execution, and AI-based analytics.

> 🧪 Designed for testability.
> ⚙️ Optimized for performance.
> 🤖 Enhanced by AI.


## 🔗 Deployed Frontend

👉 **Live App**: [Campaign Manager Frontend](https://anushkacrm.netlify.app/login)


## 🌟 Core Features

* 🔐 **Authentication & Role-Based Access** using JWT
* 📊 **Campaign and Customer Management** APIs
* 🧠 **AI Integration** using Google Gemini for message insights
* 📨 **Email Engagement Tracking** with open & click analytics
* 🧪 **Test & Simulation Endpoints** for local development
* 📦 **MongoDB** with Mongoose for fast, flexible data modeling


## 🛠️ Tech Stack

* **Node.js** & **Express.js** for scalable backend services
* **MongoDB** with **Mongoose** for schema-based data modeling
* **Google Gemini API** for AI-driven features
* **JWT** for authentication
* **Jest** for unit and integration testing
* **Dotenv**, **Morgan**, **Cors**, and more for dev and production readiness


## 🚦 Quick Start

### 1. Clone & Install

```bash
cd backend
npm install
```

### 2. Environment Setup

Copy the example config:

```bash
cp .env.example .env
```

Fill in your environment variables:

```
MONGODB_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
GEMINI_API_KEY=your_gemini_api_key
PORT=5000
```

### 3. Run the Server

```bash
npm start
```


## 🔌 API Overview

### 🔐 Authentication

* `POST /api/auth/login` – User login
* `POST /api/auth/register` – Register new user

### 📢 Campaigns

* `GET /api/campaigns` – Fetch all campaigns
* `POST /api/campaigns` – Create new campaign
* `GET /api/campaigns/:id` – Campaign details
* `GET /api/campaigns/:id/stats` – Performance stats
* `POST /api/campaigns/:id/start` – Start campaign delivery
* `POST /api/campaigns/:id/stop` – Stop campaign

### 👥 Customers

* `GET /api/customers` – Fetch all customers
* `POST /api/customers` – Add new customer
* `GET /api/customers/:id` – Customer profile

### 🧾 Orders

* `GET /api/orders` – View all orders
* `POST /api/orders` – Create order
* `GET /api/orders/:id` – Order details

### 📈 Engagement Tracking

* `GET /track/open/:campaignId/:customerId` – Email open tracker
* `GET /track/click/:campaignId/:customerId/:linkId` – Click tracking

### 🧪 Testing & Simulation

* `POST /api/test/set-random-metrics/:campaignId` – Inject test metrics
* `POST /api/test/set-random-description/:campaignId` – AI mock description


## 🤖 AI Integration

This backend uses **Google Gemini** for:

* 🧠 Generating message templates
* 📊 Creating campaign summaries
* 🔍 Offering insights based on customer behavior

To enable:

1. Generate a Gemini API key
2. Add `GEMINI_API_KEY` to `.env`
3. Restart the server


## 🧪 Testing

Run the full test suite using:

```bash
npm test
```

Unit tests cover:

* Authentication
* Campaign logic
* Input validation
* AI generation edge cases


## 📁 Project Structure

```
backend/
├── config/         # DB and server config
├── controllers/    # Request handlers
├── middleware/     # Auth, error handling, etc.
├── models/         # Mongoose schemas
├── routes/         # REST API routes
├── services/       # Core business logic
├── utils/          # Token, validation, AI helpers
└── tests/          # Jest tests
```

## 🔒 Security Highlights

* 🔐 JWT Authentication
* 🧯 Input Validation (custom + Mongoose)
* 🛡️ Rate Limiting & Secure Headers
* 🔑 Environment-based Config
* 🚫 No hardcoded secrets


## 🚀 Deployment

1. Setup MongoDB (local or cloud)
2. Fill `.env` with correct values
3. Run:

```bash
npm run build
npm start
```


## 🤝 Contribution Workflow

1. **Fork** this repository
2. Create a feature branch (`git checkout -b feat/my-feature`)
3. **Commit** your changes (`git commit -m "Add: My Feature"`)
4. Push to your fork
5. **Create a Pull Request** 🎉
