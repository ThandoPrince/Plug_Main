# Plug

Plug is a service marketplace platform that connects clients with skilled service providers, enabling users to discover services, submit requests, manage bookings, and communicate through dedicated mobile applications.

The Plug platform consists of four interconnected repositories:

## 📱 Client Application

The Plug Client Application is the mobile application used by clients to:

* Discover available services
* Browse service providers
* Request services
* Create and manage bookings
* Communicate with service providers
* Manage service requests and bookings
* Complete KYC verification

**Repository:**
[Plug Client](https://github.com/ThandoPrince/plug_app)

---

## 🧑‍🔧 Service Provider Application

The Plug Service Provider Application is the mobile application used by service providers to:

* Manage their services
* Receive service requests
* Manage bookings
* Communicate with clients
* Manage their provider profile
* Track and manage service activities
* Complete KYC verification

**Repository:**
[Plug Service Provider](https://github.com/ThandoPrince/provider_plug)

---

## ⚙️ Backend API

The Plug Backend provides the core server-side functionality for the platform, including:

* Client authentication and management
* Service provider management
* Service management
* Bookings
* Real-time communication
* Notifications
* Location and service-provider functionality
* KYC verification integration
* API services consumed by the mobile applications

The Plug Backend serves as the central communication layer between the Client Application, Service Provider Application, and AI KYC System.

**Repository:**
[Plug Backend](https://github.com/ThandoPrince/Plug_backend)

---

## 🤖 AI KYC System

The AI KYC System is a dedicated verification service used by the Plug Backend for KYC processing and verification.

The Client Application and Service Provider Application do not communicate directly with the AI KYC System. Both applications communicate with the Plug Backend, which handles KYC requests and communicates with the AI KYC System.

**Repository:**
[AI KYC System](https://github.com/ThandoPrince/plug_ai_kyc_service.git)

---

## 🏗️ Architecture

```text
┌─────────────────────────┐
│    Plug Client App      │
│       Flutter           │
└────────────┬────────────┘
             │
             │ API / WebSocket
             ▼
┌─────────────────────────┐
│      Plug Backend       │
│         Django          │
└────────────┬────────────┘
             │
             │ API / WebSocket
             ▼
┌─────────────────────────┐
│ Plug Service Provider   │
│       Flutter           │
└─────────────────────────┘


             │
             │ KYC API
             ▼
┌─────────────────────────┐
│     AI KYC System       │
│        FastAPI          │
└─────────────────────────┘
```

### Communication Flow

```text
Plug Client App ────────────┐
                            │
                            ▼
                      Plug Backend
                            │
                            │
Plug Service Provider ──────┘
       App                  │
                            │
                            ▼
                     AI KYC System
```

Both mobile applications communicate with the **Plug Backend**. The **Plug Backend is responsible for communicating with the AI KYC System** when KYC verification is required.

## 📂 Repository Structure

| Repository                                                             | Purpose                                     |
| ---------------------------------------------------------------------- | ------------------------------------------- |
| [Plug Client](https://github.com/ThandoPrince/plug_app)                | Client-facing Flutter mobile application    |
| [Plug Service Provider](https://github.com/ThandoPrince/provider_plug) | Service-provider Flutter mobile application |
| [Plug Backend](https://github.com/ThandoPrince/Plug_backend)           | Django backend API and platform services    |
| AI KYC System(https://github.com/ThandoPrince/plug_ai_kyc_service.git) | FastAPI-based KYC verification service      |


