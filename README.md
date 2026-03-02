# 🚀 CATATU Logistics Platform

**CATATU Logistics** is a digital electric commuter transport platform designed to modernize urban mobility in Nairobi and beyond.

The platform combines:

* 🚌 Structured electric transport routes
* 💳 Secure MPESA & bank-powered payments
* 📍 Real-time vehicle tracking
* 📊 Automated financial reporting & ledger accounting
* 🤖 Krypton AI (intelligent assistant for passengers, drivers & admins)

CATATU is designed to operate at the intersection of:

* Transport Infrastructure
* Financial Technology
* Real-time Location Systems
* AI-powered automation
* Investor-grade reporting

---

# 🌍 Vision

To build a clean, structured, electric commuter ecosystem that replaces informal transport inefficiencies with:

* Predictability
* Safety
* Transparency
* Financial intelligence

---

# 🏗️ System Architecture Overview

CATATU uses a **modern full-stack architecture** optimized for security, scalability, and financial integrity.

## 🔹 Frontend

* **Next.js (React Framework)**
* Hosted via Vercel or similar
* Handles:

  * Passenger booking
  * Driver interface
  * Admin dashboard
  * Krypton AI UI
  * Payment initiation (STK Push trigger)

## 🔹 Backend (Core Engine)

* **FastAPI (Python)**
* REST + WebSocket APIs
* Handles:

  * MPESA STK Push requests
  * Payment callbacks (webhooks)
  * Booking logic
  * Seat locking
  * Ledger accounting
  * Real-time vehicle tracking
  * AI prompt engine
  * Role-based authentication

## 🔹 Database

* **PostgreSQL**

  * Bookings
  * Payments
  * Ledger entries
  * Vehicles
  * Subscriptions
  * Audit logs

## 🔹 Caching & Real-Time

* **Redis**

  * Seat locks (TTL based)
  * Live vehicle location cache
  * WebSocket session handling

## 🔹 Real-Time Tracking

* **WebSockets**

  * Driver phone streams GPS coordinates
  * Passengers subscribe to vehicle updates
  * Redis stores latest vehicle position
  * PostgreSQL stores historical route tracking

## 🔹 Payments Infrastructure

### MPESA Integration

* Safaricom Daraja API (STK Push)
* Secure server-side credential storage
* Callback verification
* Idempotent transaction recording

### Bank Integration

* NCBA Business Account (Settlement & Treasury)
* Payment gateway integration for:

  * Subscriptions
  * Recurring billing
  * Bank/card payments

### Accounting Logic

* Double-entry ledger system
* Automatic revenue posting
* Balance Sheet snapshots
* Exportable CSV financial statements

---

# 💳 Payment Flow (Secure STK Push)

1. Passenger selects seat.
2. Seat is temporarily locked (5 min TTL).
3. Backend initiates MPESA STK Push.
4. Passenger enters MPESA PIN.
5. Safaricom sends callback to CATATU backend.
6. Backend verifies:

   * Amount
   * Reference
   * Receipt number
7. Payment recorded.
8. Ledger entry posted.
9. Booking confirmed.
10. Receipt generated.

No manual MPESA reference entry required.

---

# 📊 Financial Engine

CATATU includes an embedded accounting layer:

### Accounts Used

* Cash
* Ride Revenue
* Deferred Revenue (subscriptions)
* Accounts Payable
* Owner’s Equity
* Operating Expenses

### Features

* Automatic journal entries
* Revenue computation from ledger (not bookings)
* Balance Sheet generation
* CSV export
* Daily revenue summaries
* Settlement reconciliation vs NCBA bank

This ensures investor-grade financial visibility.

---

# 📍 Real-Time Vehicle Tracking

Driver app sends GPS coordinates every 2–5 seconds.

### Flow

Driver Phone → WebSocket → Backend → Redis → Passenger Map

### Stored Data

* Live location (Redis)
* Historical trip route (PostgreSQL)
* Trip performance analytics

Passengers can:

* View bus/van live location
* Track estimated arrival time
* Receive trip notifications

---

# 🤖 Krypton AI

Krypton AI is CATATU’s intelligent assistant.

It operates in two domains:

## Passenger Assistant

* Booking guidance
* Receipt retrieval
* Trip status clarification
* Support triage

## Admin Assistant

* Daily revenue summary
* Financial insights
* Suspicious transaction detection
* Weekly investor report drafting

## Security Guardrails

* Krypton AI cannot access payment secrets.
* Cannot alter financial records.
* Cannot approve refunds without admin confirmation.
* All outputs are logged for audit.

Krypton AI uses structured prompts and controlled input schemas to prevent hallucinations and financial errors.

---

# 🔐 Security Model

* All payment secrets are stored in environment variables.
* HTTPS-only endpoints.
* Webhook validation & idempotency checks.
* Role-Based Access Control (RBAC).
* Audit logs for financial operations.
* No sensitive keys stored in frontend.
* Data Protection Act (Kenya) compliance alignment.

---

# 🗂️ Project Structure

```
catatu-platform/
│
├── frontend/ (Next.js)
│   ├── passenger
│   ├── driver
│   ├── admin
│   └── krypton-ui
│
├── server/ (FastAPI Backend)
│   ├── app/
│   │   ├── main.py
│   │   ├── payments/
│   │   ├── bookings/
│   │   ├── tracking/
│   │   ├── ledger/
│   │   ├── krypton/
│   │   └── auth/
│   ├── requirements.txt
│   └── .env
│
└── README.md
```

---

# 🚦 Development Roadmap

## Phase 1 (Core Launch)

* Booking + Seat Locking
* MPESA STK Push
* Ledger + Receipts
* Basic tracking
* Admin revenue export

## Phase 2 (Scale)

* Subscriptions
* Bank settlement reconciliation
* Driver app optimization
* Enhanced analytics

## Phase 3 (Intelligence Layer)

* Krypton AI full deployment
* Predictive occupancy
* Route optimization
* Dynamic pricing
* Automated investor reports

---

# 🏦 Banking & Settlement

CATATU operates under a registered company structure.

Funds flow:

MPESA / Gateway → Settlement → NCBA Business Account

Backend reconciles:

* Ledger revenue
* MPESA receipts
* Bank deposits

---

# 🛠️ Tools & Technologies

| Layer         | Tool                                   |
| ------------- | -------------------------------------- |
| Frontend      | Next.js                                |
| Backend       | FastAPI                                |
| Database      | PostgreSQL                             |
| Cache         | Redis                                  |
| Payments      | Safaricom Daraja API                   |
| Subscriptions | Payment Gateway (Flutterwave/Paystack) |
| Hosting       | Render / Fly.io / Vercel               |
| Realtime      | WebSockets                             |
| AI            | Krypton AI Prompt Engine               |

---

# 📈 Designed For

* Scalable transport operations
* Clean energy transition
* Institutional capital readiness
* Investor reporting transparency
* Enterprise-grade accounting compliance

---

# ⚖ Legal & Compliance

* Registered company operations
* Business bank account (NCBA)
* MPESA Paybill integration
* Data Protection compliance
* Transaction record retention policy

---

# 🧠 Philosophy

CATATU is not just a transport booking system.

It is:

* A structured mobility infrastructure.
* A fintech-grade transaction engine.
* A real-time fleet intelligence platform.
* An AI-augmented transport ecosystem.

---

# 🧑‍💻 Author

Co-Founder & CFO: Ben Kyaka
Electric Mobility Infrastructure | FinTech | Systems Architecture

---


