# .github
Backend API for East African transport routes, schedules, and bookings, FastAPI + MongoDB backend for East African mobility and transport data
# Jakasipul Core: Mobility API 🌍🚌

The foundational high-performance backend engine powering East African transport systems, route optimization, transit scheduling, and digital ticket booking. Built using **FastAPI** and **MongoDB**.

## 🚀 System Overview

This core service manages high-concurrency mobility data across East African transit networks. By pairing FastAPI’s asynchronous capabilities with MongoDB's flexible, geospatial-ready document model, the platform easily processes complex regional data structures—ranging from inter-city bus routes (e.g., Nairobi to Kampala) to localized transit schedules.

### 🛠️ Tech Stack
*   **Framework:** FastAPI (Python 3.11+)
*   **Database:** MongoDB (using Motor for async ODM/driver support)
*   **Validation:** Pydantic v2
*   **Containerization:** Docker / Docker Compose

---

## 🏗️ Core API Architecture & Features

*   **Geospatial Routing Engine:** Utilizes MongoDB 2dsphere indexes to track route coordinate paths, coordinates, and calculate proximity matching for transit stops.
*   **Dynamic Scheduling Engine:** Asynchronous pipelines handle matrix schedules across varying timezones and cross-border transport nodes.
*   **Atomic Booking System:** Protects transaction boundaries during booking stages to prevent double-seat allocation on passenger buses, trains, and shuttles.

---

## 📂 Project Structure

```text
├── app/
│   ├── api/                # API router entry points (v1)
│   │   ├── endpoints/      # Routes: /routes, /schedules, /bookings
│   ├── core/               # App configuration, security, and database clients
│   ├── models/             # MongoDB / Pydantic data schemas
│   ├── services/           # Business logic (fare computation, booking processing)
│   └── main.py             # FastAPI application setup and lifecycle events
├── tests/                  # Pytest validation suites
├── .env.example            # Environment variables template
├── docker-compose.yml      # Local development environment mesh
└── Requirements.txt        # Application dependencies
