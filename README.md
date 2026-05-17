<!--
**DevEsraaMahmoud/DevEsraaMahmoud** is a ✨ special ✨ repository because its README.md appears on your GitHub profile.
-->

# Hi, I'm Esraa 👋

Senior Full-Stack Engineer with a strong backend and product mindset.  
I specialize in building scalable, production-ready systems using Laravel and modern web technologies.

---

## Metrics

![Metrics](./github-metrics.svg)

---

## 🔥 Contribution Streak

<p align="center">
  <img 
    src="https://streak-stats.demolab.com?user=DevEsraaMahmoud&theme=tokyonight&hide_border=true" 
  />
</p>

---

## 🛠 Workflow & Tooling

<p>
  <img src="https://img.shields.io/badge/Laravel-red?style=for-the-badge&logo=laravel&logoColor=white"/>
  
  <img src="https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white"/>
  
  <img src="https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vue.js&logoColor=4FC08D"/>
  
  <img src="https://img.shields.io/badge/MySQL-black?style=for-the-badge&logo=mysql"/>
  
  <img src="https://img.shields.io/badge/Redis-red?style=for-the-badge&logo=redis&logoColor=white"/>
  
  <img src="https://img.shields.io/badge/Docker-black?style=for-the-badge&logo=docker"/>
  
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white"/>
</p>

---

## 🔧 Tech Focus

- Backend: **PHP (Laravel), REST APIs, Event-driven systems**
- Databases: **MySQL (indexing, EXPLAIN, optimization)**
- Performance: **Redis caching, queues, async processing**
- Integrations: **Payments, webhooks, B2B APIs**
- Frontend: **Vue.js, Inertia.js, Livewire**
- Infrastructure: **Docker, Nginx, CI/CD basics**

---

## ⚙ Engineering Interests

- System Design & Scalability
- Performance Optimization
- Distributed Systems Concepts
- Queues & Async Workflows
- Backend Architecture
- Testing & Debugging
- CI/CD Automation

---

## 🚀 Featured Projects

---

### 🔹 Laravel Million Users

High-performance system for 1M+ records with optimized search and batch processing.

![Laravel](https://img.shields.io/badge/Laravel-red)
![MySQL](https://img.shields.io/badge/MySQL-FULLTEXT-black)
![Redis](https://img.shields.io/badge/Redis-Cache-red)

#### 🧱 Architecture

```mermaid
flowchart TD
    subgraph Client
        A[API / Web Client]
    end

    subgraph App["Laravel Application"]
        B[Search Controller]
        C{Cache Layer}
        D[Query Optimizer]
        E[Queue Dispatcher]
    end

    subgraph Workers
        F[Batch Import Job]
        G[Index / Aggregate Job]
    end

    subgraph Data
        H[(Redis Cache)]
        I[(MySQL — 1M+ rows)]
        J[FULLTEXT Index]
    end

    A --> B
    B --> C
    C -->|miss| D
    C -->|hit| H
    D --> J
    J --> I
    D --> H
    B --> E --> F
    F --> I
    E --> G --> J
```

#### ⚡ Highlights
- MySQL FULLTEXT search at scale
- Redis caching for hot queries
- Queue-based batch imports & indexing
- EXPLAIN-driven query optimization

🔗 https://github.com/DevEsraaMahmoud/laravel-million-users

---

### 🔹 Payment Integration Demo

Production-style payment processing with secure webhooks, idempotent flows, and async verification.

![Laravel](https://img.shields.io/badge/Laravel-11-red)
![PHP](https://img.shields.io/badge/PHP-8.3-blue)
![Redis](https://img.shields.io/badge/Redis-Queues-red)
![Tests](https://github.com/DevEsraaMahmoud/payment-integration-demo/actions/workflows/tests.yml/badge.svg)

#### 🧱 Architecture

```mermaid
flowchart LR
    subgraph Client
        A[Checkout / Client App]
    end

    subgraph Backend["Laravel API"]
        B[Payment Controller]
        C[Payment Service]
        D[Gateway Abstraction]
        E[Webhook Handler]
        F[Idempotency Layer]
    end

    subgraph External
        G[(Stripe / PayMob)]
    end

    subgraph Async
        H[(Redis Queue)]
        I[Verify Payment Job]
    end

    subgraph Storage
        J[(MySQL)]
    end

    A --> B --> C --> D --> G
    G -->|Webhook| E
    E --> F --> H --> I --> J
    C --> J
```

#### ⚡ Highlights
- Idempotent payment processing
- Secure webhook validation
- Retry-safe queue-based verification
- Transaction logging & failure recovery

🔗 https://github.com/DevEsraaMahmoud/payment-integration-demo

---

### 🔹 PingMe — Real-Time Communication

Real-time messaging with presence, typing indicators, and event broadcasting.

![Laravel Reverb](https://img.shields.io/badge/Laravel-Reverb-red)
![Vue](https://img.shields.io/badge/Vue-3-4FC08D)
![Redis](https://img.shields.io/badge/Redis-PubSub-red)
![Tests](https://github.com/DevEsraaMahmoud/PingMe/actions/workflows/tests.yml/badge.svg)

#### 🧱 Architecture

```mermaid
flowchart TB
    subgraph Frontend["Vue 3 + Inertia"]
        A[Chat UI]
        B[Presence / Typing State]
    end

    subgraph Realtime["Laravel Reverb"]
        C[WebSocket Server]
        D[Channel Authorization]
    end

    subgraph Backend["Laravel Backend"]
        E[Message API]
        F[Broadcast Events]
        G[Presence Service]
    end

    subgraph Infra
        H[(Redis Pub/Sub)]
        I[(MySQL)]
    end

    A <-->|WebSocket| C
    B <-->|WebSocket| C
    C --> D
    E --> F --> H
    H --> C
    E --> I
    G --> H
    A -->|HTTP| E
```

#### ⚡ Highlights
- WebSocket real-time messaging
- Presence & typing indicators
- Redis pub/sub for horizontal scaling
- Event-driven broadcast pipeline

🔗 https://github.com/DevEsraaMahmoud/PingMe

---


## 🧠 How I Think

- Start from the **problem**, not the framework
- Prefer **simple architectures** that can evolve
- Measure before optimizing
- Care about trade-offs and real business impact

---

## 📫 Get in Touch

- LinkedIn: https://linkedin.com/in/esraa-mahmoud
