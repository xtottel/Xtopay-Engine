## 📘 `xtopay-engine`

**Xtopay Engine** is a modular, high-performance payment processing engine tailored for Ghanaian payment infrastructure. It supports Mobile Money, card payments, bank transfers, local wallet schemes, and national switches.

---

### 🚀 Core Features

* 🇬🇭 **Ghana-first integrations**

  * MTN, Vodafone, AirtelTigo (MoMo)
  * GhIPSS, Gh-Link, Ezwich
  * Visa, MasterCard
  * Absa, G-Money, Hubtel, Zeepay
* 🔌 Pluggable payment connectors
* 📤 Smart routing & fallback strategies
* 💸 Reconciliation & settlement handling
* ⚠️ Risk & fraud detection engine
* 📡 Notification + event system (SMS, email, webhooks)
* 📊 Logging, metrics, tracing (Prometheus + Grafana)

---

### 🧱 Monorepo Structure

```
xtopay-engine/
├── packages/         # Core modules
│   ├── core-engine/      # Routing, auth, settlement
│   ├── connectors/       # MoMo, cards, banks, wallets
│   ├── risk/             # Fraud detection & rules
│   ├── api-adapters/     # APIs for merchant, admin, client
│   ├── shared/           # Common types, config, logs, events
├── services/         # Microservices
│   ├── transaction-service/
│   ├── reconciliation-service/
│   └── notification-service/
├── infrastructure/   # Gateway, configs, monitoring
├── scripts/          # Migrations, deploy scripts
└── README.md
```

---

### 🛠️ Getting Started

#### 📦 Prerequisites

* Node.js `>=18`
* Yarn or PNPM
* PostgreSQL
* Redis
* Docker (optional, for local services)

#### 🚀 Local Setup

```bash
# 1. Clone the repo
git clone https://github.com/xtottel/xtopay-engine.git && cd xtopay-engine

# 2. Install dependencies
pnpm install

# 3. Setup environment
cp .env.example .env
# Update credentials and API keys for test environments

# 4. Run services
pnpm dev
```

---

### 📁 Key Modules

| Module         | Purpose                                           |
| -------------- | ------------------------------------------------- |
| `core-engine`  | Handles authorization, routing, settlement        |
| `connectors`   | Integrations for MoMo, GhIPSS, Absa, Visa, etc.   |
| `risk`         | Velocity checks, fraud detection, rules           |
| `api-adapters` | REST interfaces for dashboard & partners          |
| `shared`       | Common types, telemetry, messaging                |
| `services`     | Transaction, reconciliation, notification workers |

---

### 🧪 Testing

```bash
# Run unit tests
pnpm test

# Run specific service test
pnpm --filter transaction-service test
```

---

### 📡 Monitoring & Instrumentation

* `Prometheus` for metrics
* `Grafana` dashboards under `/infrastructure/monitoring/grafana/`
* `OpenTelemetry` ready in `shared/instrumentation`

---

### 📤 Deployment

Provisioning is automated via:

* `scripts/provisioning/terraform/`
* `scripts/deploy.sh` (customizable)

You can target:

* AWS (ECS/Fargate)
* Railway
* GCP (Cloud Run)
* Render (for small scale)

---

### 👥 Contributing

We welcome contributions!

```bash
# Create a feature branch
git checkout -b feat/add-ghipss-logs

# Commit changes
git commit -m "feat: add transaction logging for ghipss"

# Push and open PR
git push origin feat/add-ghipss-logs
```

Make sure your code:

* Passes lint checks: `pnpm lint`
* Includes unit or integration tests
* Uses types and shared utilities from `packages/shared`

---

### 🧩 Environment Variables

```env
DATABASE_URL=
REDIS_URL=
MTN_API_KEY=
VODAFONE_SECRET=
VISA_PUBLIC_KEY=
HUBTEL_CLIENT_ID=
GHPASS_SIGNING_KEY=
REGION=gh
```

See `.env.example` for the full list.

---

### 🧠 Roadmap

* [x] Ghana-only payment engine (MoMo, cards, wallets)
* [ ] Add international fallback (Stripe, Paystack)
* [ ] Multi-currency FX routing
* [ ] Full PCI DSS scope (for card tokenization)
* [ ] ISO 27001-aligned audit system

---

### 📬 Contact

For questions, integrations, or partnership requests:

> **Collins Joe** — CEO, Xtottel Technologies
> 📩 `collins@xtottel.com`
> 🌐 [xtopay.co](https://xtopay.co)

---