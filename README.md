# Plug

Plug is a service marketplace platform that connects clients with skilled service providers, enabling users to discover services, submit requests, manage bookings, and communicate through dedicated mobile applications.

The Plug platform consists of three interconnected repositories:

## 📱 Client Application

The Plug Client Application is the mobile application used by clients to:

* Discover available services
* Browse service providers
* Request services
* Create and manage bookings
* Communicate with service providers
* Manage service requests and bookings

**Repository:**
[https://github.com/ThandoPrince/plug_app.git]

---

## 🧑‍🔧 Service Provider Application

The Plug Service Provider Application is the mobile application used by service providers to:

* Manage their services
* Receive service requests
* Manage bookings
* Communicate with clients
* Manage their provider profile
* Track and manage service activities

**Repository:**
[https://github.com/ThandoPrince/provider_plug.git]

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
* API services consumed by the mobile applications

**Repository:**
[(https://github.com/ThandoPrince/Plug_backend.git)]

---

## 🏗️ Architecture

```text
                 ┌─────────────────────────┐
                 │    Plug Client App      │
                 │       Flutter           │
                 └────────────┬────────────┘
                              │
                              │ API / WebSocket
                              │
                 ┌────────────▼────────────┐
                 │      Plug Backend       │
                 │         Django          │
                 └────────────▲────────────┘
                              │
                              │ API / WebSocket
                              │
                 ┌────────────┴────────────┐
                 │ Plug Service Provider   │
                 │       Flutter           │
                 └─────────────────────────┘
```

## 📂 Repository Structure

| Repository            | Purpose                             |
| --------------------- | ----------------------------------- |
| Plug Client           | Client-facing mobile application    |
| Plug Service Provider | Service-provider mobile application |
| Plug Backend          | Backend API and platform services   |

## 🔗 Related Repositories

* **Client Application:** [Repository Link]
* **Service Provider Application:** [Repository Link]
* **Backend API:** [Repository Link]
