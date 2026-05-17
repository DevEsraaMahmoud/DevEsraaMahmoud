<!--
**DevEsraaMahmoud/DevEsraaMahmoud** is a ✨ special ✨ repository because its README.md appears on your GitHub profile.
-->

# Hi, I'm Esraa 👋

Senior Full-Stack Engineer with a strong backend and product mindset.  
I build scalable, production-ready systems with **Laravel** and modern web stacks.

## 🔧 Tech Focus

<p>
  <img src="https://img.shields.io/badge/Backend-Laravel-FF2D20?style=flat-square&logo=laravel&logoColor=white"/>
  <img src="https://img.shields.io/badge/REST-API-512BD4?style=flat-square"/>
  <img src="https://img.shields.io/badge/Event--driven-181717?style=flat-square"/>
  <img src="https://img.shields.io/badge/Data-MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white"/>
  <img src="https://img.shields.io/badge/Indexing%20%26%20Optimization-2E7D32?style=flat-square"/>
  <img src="https://img.shields.io/badge/Performance-Redis-DC382D?style=flat-square&logo=redis&logoColor=white"/>
  <img src="https://img.shields.io/badge/Queues-FF6F00?style=flat-square"/>
  <img src="https://img.shields.io/badge/Async-Processing-5C6BC0?style=flat-square"/>
  <img src="https://img.shields.io/badge/Payments-00897B?style=flat-square"/>
  <img src="https://img.shields.io/badge/Webhooks-6A1B9A?style=flat-square"/>
  <img src="https://img.shields.io/badge/B2B-APIs-1565C0?style=flat-square"/>
  <img src="https://img.shields.io/badge/Frontend-Vue-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white"/>
  <img src="https://img.shields.io/badge/Inertia-9553E9?style=flat-square"/>
  <img src="https://img.shields.io/badge/Livewire-FB70A9?style=flat-square"/>
  <img src="https://img.shields.io/badge/Infra-Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white"/>
  <img src="https://img.shields.io/badge/CI%2FCD-2088FF?style=flat-square&logo=githubactions&logoColor=white"/>
</p>

## ⚙ Engineering Interests

<p>
  <img src="https://img.shields.io/badge/System%20Design-181717?style=flat-square"/>
  <img src="https://img.shields.io/badge/Scalability-0D47A1?style=flat-square"/>
  <img src="https://img.shields.io/badge/Distributed%20Systems-4A148C?style=flat-square"/>
  <img src="https://img.shields.io/badge/Queues%20%26%20Async-FF6F00?style=flat-square"/>
  <img src="https://img.shields.io/badge/Backend%20Architecture-37474F?style=flat-square"/>
  <img src="https://img.shields.io/badge/Performance-C62828?style=flat-square"/>
  <img src="https://img.shields.io/badge/Testing-2E7D32?style=flat-square"/>
  <img src="https://img.shields.io/badge/CI%2FCD-2088FF?style=flat-square&logo=githubactions&logoColor=white"/>
</p>

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
