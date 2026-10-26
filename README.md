# Plug

Plug is a service marketplace platform that connects clients with skilled service providers, enabling users to discover services, submit requests, manage bookings, and communicate through dedicated mobile applications.

The Plug platform consists of four interconnected repositories, supported by a backend API and an AI-powered KYC verification system.

## 🎥 Demo Video

Watch the Plug platform demonstration to see how clients and service providers interact with the platform, from discovering services and managing bookings to completing service sessions.

**Demo Video:** [Watch the Plug Demo](https://1drv.ms/v/c/c9e3a0df5f41360f/IQDSxWHwiqXRTrzUaZ3M3pmvAbKxa_iD_TXDybJhdvUkTEk?e=Cj3m0Q)

## 📲 Mobile Applications

### Client Application

The Plug Client Application enables clients to:

N.B! Only runs on Android

- Discover available services.
- Browse service providers.
- Request services and negotiate prices.
- Create and manage bookings.
- Communicate with service providers.
- Track service activities.
- Complete KYC verification.

**Links:**
- **Source Code:** [Plug Client Repository](https://github.com/ThandoPrince/plug_app)
- **Download App:** [Plug Client App](https://1drv.ms/u/c/c9e3a0df5f41360f/IQDFX4zrKE5GT5th-oZAxpUsASchoBDfeU_pwdI_r2-wyn0?e=yUqgGM)

---

### 🧑‍🔧 Service Provider Application
N.B! Only runs on Android
The Plug Service Provider Application enables service providers to:

- Create and manage their services.
- Receive and respond to service requests.
- Negotiate prices and manage bookings.
- Communicate with clients.
- Manage their provider profiles.
- Track and manage service activities.
- Complete KYC verification.
- Confirm service completion and rate clients.

**Links:**
- **Source Code:** [Plug Service Provider Repository](https://github.com/ThandoPrince/provider_plug)
- **Download App:** [Plug Service Provider App](https://1drv.ms/u/c/c9e3a0df5f41360f/IQCNYsGhyNNlS5qBc7M8GoQVATCI44TpT2k__XPsIFM11dM?e=oc8FqF)

---

## ⚙️ Backend API

The Plug Backend provides the core server-side functionality for the platform, including:

- Client authentication and management.
- Service provider management.
- Service management.
- Booking and negotiation workflows.
- Real-time communication.
- Notifications.
- Location and service-provider functionality.
- KYC verification integration.
- API services consumed by the mobile applications.

The backend serves as the central communication layer between the Client Application, Service Provider Application, and AI KYC System.

**Repository:** [Plug Backend](https://github.com/ThandoPrince/Plug_backend)

---

## 🤖 AI KYC System

The AI KYC System is a dedicated verification service used by the Plug Backend for identity verification and KYC processing.

The Client Application and Service Provider Application do not communicate directly with the AI KYC System. Both applications communicate with the Plug Backend, which processes KYC requests and communicates with the AI KYC System.

**Repository:** [AI KYC System](https://github.com/ThandoPrince/plug_ai_kyc_service)

---

## 🏗️ System Architecture

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
                            ├──────────► AI KYC System
                            │
Plug Service Provider ──────┘
         App
```

Both mobile applications communicate with the **Plug Backend**. The backend handles communication with the AI KYC System whenever identity verification is required.

---

## 📂 Repository Structure

| Repository | Purpose |
|---|---|
| [Plug Client](https://github.com/ThandoPrince/plug_app) | Client-facing Flutter mobile application |
| [Plug Service Provider](https://github.com/ThandoPrince/provider_plug) | Service-provider Flutter mobile application |
| [Plug Backend](https://github.com/ThandoPrince/Plug_backend) | Django backend API and platform services |
| [AI KYC System](https://github.com/ThandoPrince/plug_ai_kyc_service) | FastAPI-based KYC verification service |

---

## 🛠️ Technology Stack

- **Mobile Applications:** Flutter / Dart
- **Backend API:** Django / Django REST Framework
- **AI KYC Service:** FastAPI
- **Communication:** REST API / WebSockets
- **Authentication:** JWT and OTP-based verification

