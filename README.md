<div align="center">

# André Luiz Gonçalves

**Software Engineer · Java / Spring Boot · React**

*Building production-grade distributed systems at [Gentek.ai](https://gentek.ai) · Lisbon, Portugal*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/andr%C3%A9-luiz-b9915b275/)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=flat&logo=astro&logoColor=white)](https://myportfolio.beyouweb.com/)
[![Beyou Docs](https://img.shields.io/badge/BeYou_Docs-0082E1?style=flat&logo=readthedocs&logoColor=white)](https://docs.beyouweb.com)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:andreluizgoncalves741@gmail.com)

</div>

---

## About

Software Engineer focused on backend-heavy full-stack development, distributed systems and performance engineering. Currently evolving an AI SaaS platform used by banking clients, from OLAP data pipelines and reactive microservices to modular React frontends.

Outside work I build and operate [Beyou](https://beyouweb.com), a gamified habit manager running as a real production: web, native mobile, an AI agent, and infrastructure I host and monitor myself.

I care about systems that work correctly *in production*: observable, testable, resilient, and built to scale before the problems become visible.

---

## Stack

<div align="center">

**Backend**

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat&logo=spring-boot&logoColor=white)
![Spring WebFlux](https://img.shields.io/badge/Spring_WebFlux-6DB33F?style=flat&logo=spring&logoColor=white)
![Apache Kafka](https://img.shields.io/badge/Apache_Kafka-231F20?style=flat&logo=apache-kafka&logoColor=white)

**Frontend**

![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)
![React Native](https://img.shields.io/badge/React_Native-20232A?style=flat&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Redux](https://img.shields.io/badge/Redux-764ABC?style=flat&logo=redux&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat&logo=tailwind-css&logoColor=white)

**Data & Infrastructure**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![StarRocks](https://img.shields.io/badge/StarRocks-FF6B00?style=flat&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazon-aws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat&logo=grafana&logoColor=white)

**Testing & Quality**

![JUnit 5](https://img.shields.io/badge/JUnit_5-25A162?style=flat&logo=junit5&logoColor=white)
![Testcontainers](https://img.shields.io/badge/Testcontainers-291A3F?style=flat&logo=testcontainers&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat&logo=playwright&logoColor=white)
![k6](https://img.shields.io/badge/k6-7D64FF?style=flat&logo=k6&logoColor=white)

</div>

---

## Selected Work

### Production Engineering @ Gentek.ai

A few highlights from building a financial-grade AI SaaS platform:

| What | Result |
|------|--------|
| **StarRocks OLAP migration** — moved EMIR/SFTR analytics layer from PostgreSQL to StarRocks with incremental MV refresh | Processing data pipeline: 1 hour → **2.1s** · MV refresh flat at ~14s regardless of data volume · endpoint p50 −92% |
| **Distributed L1/L2 cache** — Caffeine + Redis/Redisson with cross-pod pub/sub invalidation and ACL-scoped keys | −67% p95 · +101% throughput · latency cut to 1/3 |
| **Load testing campaign with k6** — caught OOM at 92% heap and I/O bottlenecks before first client go-live | +681% throughput · −91% p95 after optimisation |
| **E2E contract testing engine** — internal Java 21 service with virtual threads, SSE and multi-environment UI | Caught real cache bugs on day one that 80% unit coverage had missed |
| **Test coverage 0% → 80%** across 4 critical microservices | JUnit 5 · Mockito · Testcontainers · integrated in CI/CD |
| **Reactive notification service** — fully non-blocking stack with WebFlux + R2DBC + reactor-kafka + AWS MSK | Priority-based processing · deduplication · real-time SSE streaming |

---

## Personal Project

### [Beyou](https://app.beyouweb.com) — Gamified Habit & Routine Manager

A free, open-source life manager I run as a real production: live web app, native Android app, and a public engineering docs site, all served from infrastructure I built and operate myself.

**[Live app](https://app.beyouweb.com)** · **[Engineering docs & blog](https://docs.beyouweb.com)** · **[Backend source](https://github.com/AndDev741/Beyou-backend-spring)**

| What | How |
|------|-----|
| **One TypeScript core, two clients** | React web + React Native (Expo) in a Turborepo monorepo — state, API layer, validation, i18n and themes shared as source, so one edit hot-reloads both apps |
| **AI agent with 33 tools** | Spring AI agent that operates the user's real data over SSE, on a fallback chain of free-tier LLMs (Mistral → Gemini → GLM → DeepSeek) — running cost so far: $0 |
| **Self-hosted production** | Cloudflare Tunnel with zero open ports, GHCR images auto-deployed by Watchtower, a Playwright e2e suite gating CI |
| **Full observability** | Prometheus + Grafana dashboards, Loki logs, self-hosted GlitchTip error tracking with uptime and heartbeat monitors — same stack in dev and prod |
| **Gamified domain engine** | Server-side XP curve, levels and streaks · Caffeine caching · Flyway-owned schema · JWT + Google OAuth |

I write about the engineering on the [docs site](https://docs.beyouweb.com): the free-tier LLM cascade, a security audit run with an AI agent, the monitoring layers, and what self-hosting on a 2012 laptop actually costs.

---

<img src="https://raw.githubusercontent.com/AndDev741/AndDev741/output/snake.svg" alt="Snake animation" />

---

<div align="center">

*Currently solving problems in distributed systems, performance engineering and financial data.*

</div>
