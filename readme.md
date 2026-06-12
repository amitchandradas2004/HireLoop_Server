# 🚀 HireLoop Server

Backend API for HireLoop, a modern job marketplace platform that connects Job Seekers and Recruiters through a secure, scalable, and role-based recruitment system.

## 📖 Overview

HireLoop Server powers the core functionality of the HireLoop platform, including authentication, authorization, company management, job management, applicant tracking, subscriptions, payments, and analytics.

Built with Node.js, Express.js, MongoDB, JWT, and Stripe.

---

## ✨ Features

### 🔐 Authentication & Authorization

- JWT Authentication
- Role-Based Access Control (RBAC)
- Protected Routes
- Password Hashing with bcrypt
- Secure User Sessions

### 👤 User Management

- User Registration
- User Login
- Profile Management
- Role Assignment
- Account Suspension & Activation

### 🏢 Company Management

- Company Registration
- Company Approval Workflow
- Company Profile Updates
- Company Status Management

### 💼 Job Management

- Create Jobs
- Update Jobs
- Delete Jobs
- Close/Reopen Jobs
- Job Search & Filtering
- Active Job Limit Enforcement

### 📄 Application Management

- Submit Applications
- Track Application Status
- Resume Management
- Applicant Tracking

### 💳 Subscription & Billing

- Subscription Management
- Stripe Payment Integration
- Upgrade/Downgrade Plans
- Payment History
- Revenue Tracking

### 📊 Analytics

- User Analytics
- Company Analytics
- Job Analytics
- Revenue Analytics
- Subscription Analytics

---

## 👥 User Roles

### Seeker

- Manage Profile
- Apply for Jobs
- Save Jobs
- Track Applications
- Manage Subscription

### Recruiter

- Register Company
- Manage Company
- Create Jobs
- Manage Jobs
- Review Applicants
- Manage Subscription

### Admin

- Manage Users
- Manage Companies
- Manage Jobs
- Manage Payments
- View Analytics

---

## 📄 Application Status Flow

```text
Applied
   ↓
Under Review
   ↓
Shortlisted
   ↓
Offered / Rejected
```

| Status | Description |
|----------|------------|
| Applied | Application submitted |
| Under Review | Recruiter reviewing application |
| Shortlisted | Candidate selected for interview |
| Rejected | Application declined |
| Offered | Job offer sent |

---

## 🏢 Company Approval Workflow

```text
Pending
   ↓
Admin Review
 ↙       ↘
Approved Rejected
```

---

## 💳 Subscription Plans

### Seeker Plans

| Plan | Application Limit |
|--------|------------------|
| Free | 3 Applications / Month |
| Pro | 30 Applications / Month |
| Premium | Unlimited Applications |

### Recruiter Plans

| Plan | Active Job Limit |
|--------|-----------------|
| Free | 3 Active Jobs |
| Growth | 10 Active Jobs |
| Enterprise | 50 Active Jobs |

---

## 🛠️ Tech Stack

### Backend

- Node.js
- Express.js

### Database

- MongoDB

### Authentication

- JWT


### Payments

- Stripe

### Deployment

- Render
- MongoDB Atlas

---

## 🔑 Environment Variables

```env
PORT=5000

DB_URI=your_mongodb_connection_string

JWT_SECRET=your_jwt_secret

STRIPE_SECRET_KEY=your_stripe_secret_key

CLIENT_URL=http://localhost:5173
```

---

## 📡 API Modules

### Authentication

```http
POST /api/auth/register
POST /api/auth/login
```

### Users

```http
GET    /api/users
GET    /api/users/:id
PATCH  /api/users/:id
```

### Companies

```http
POST   /api/companies
GET    /api/companies
PATCH  /api/companies/:id
```

### Jobs

```http
POST   /api/jobs
GET    /api/jobs
GET    /api/jobs/:id
PATCH  /api/jobs/:id
DELETE /api/jobs/:id
```

### Applications

```http
POST   /api/applications
GET    /api/applications
PATCH  /api/applications/:id
```

### Payments

```http
POST   /api/create-payment-intent
GET    /api/payments
```

---

## 🔒 Security Features

- JWT Authentication
- Role-Based Authorization
- Protected API Endpoints
- Password Hashing
- Environment Variable Protection
- Stripe Secure Payments

---

## 👨‍💻 Developer

**Amit**

Full-Stack Web Developer

---

## 📜 License

This project is licensed under the MIT License.