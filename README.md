<h1 align="center">Hi, I'm Achraf Rejouan</h1>
<h3 align="center">Backend Engineer · Distributed Systems · Event-Driven Architecture · Tunisia</h3>

<p align="center">
  <strong>Licence Appliquée en Informatique</strong> (Information Systems Development), ISET Zaghouan — graduated with Excellent distinction.<br/>
  I build backend systems in <strong>Java 21 / Spring Boot 3</strong> with <strong>Kafka</strong>, <strong>PostgreSQL</strong> and <strong>Redis</strong>,<br/>
  and I care about what they do under concurrency and failure — measured, not asserted.
</p>

<p align="center">
  <a href="https://achrafrejouan.vercel.app/">Portfolio</a> ·
  <a href="https://linkedin.com/in/achraf-rejouan">LinkedIn</a> ·
  <a href="mailto:achrafrejouan@gmail.com">achrafrejouan@gmail.com</a>
</p>

---

## Selected work

**[Wassal](https://github.com/Achraf-Rejouan/wassal)** — real-time courier dispatch engine · `Java 21` `Spring Boot 3` `Kafka` `Redis` `PostgreSQL/PostGIS`

Five services behind a transactional outbox. Four of six correctness invariants are enforced by partial unique indexes rather than by application code, so the database refuses the bad state instead of trusting a check.

| Claim | Measured |
|---|---|
| No double assignment | 5,000 concurrent accepts / 50 couriers → **0 violations** |
| One winner per order | 40 couriers racing one order → **exactly 1** |
| Recovery after `SIGKILL` | **6.1 s** vs a 30 s target, **0 orders lost** |
| Offer expiry after a crash mid-offer | fired **0.134 s** past deadline vs a ±1 s target |

Integration, concurrency and chaos suites run against real Postgres, Redis and Kafka via Testcontainers and Toxiproxy in CI. No infrastructure is mocked anywhere — an ArchUnit rule enforces it. `./wassal.sh demo` reproduces every claim in the README, misses included.

**[TalentMatcher](https://github.com/Achraf-Rejouan/Talent_Matcher)** — AI recruitment platform (final graduation project) · `Java` `Spring Boot` `Kafka` `Oracle XE 21c` `Angular 17`

Six Spring Boot microservices communicating over Kafka, schema-per-service on Oracle XE 21c, secured with Keycloak (OAuth2/PKCE, JWT, RBAC). An SBERT semantic matching engine scores candidates against job requirements and returns an explainable breakdown rather than an opaque number. 77 automated tests across four Scrum sprints.

**[IDAP](https://github.com/Achraf-Rejouan/ISET-Decisional-Analytics-Platform-IDAP)** — academic BI / data-warehouse platform, deployed to production · `NestJS` `Next.js` `PostgreSQL`

The full decisional chain: append-only event log → immutable staging → scheduled ETL → Kimball star schema with SCD Type 2 dimensions → data marts across five grains → drill-down BI dashboards. Every published figure is recomputed from staging on each run; a failed reconciliation withholds the mart instead of publishing wrong numbers. **285,000 events** rebuilt deterministically in **46 s**; dashboard query latency cut from **788 ms to 7 ms**.

Also on this profile: **[fa-dhakker](https://github.com/Achraf-Rejouan/fa-dhakker)** — a step-by-step Islamic prayer learning application (Next.js, TypeScript).

---

## Currently

- Deep-diving into **distributed systems**, **correctness under failure**, and **data-warehouse design**
- Certified: **ISTQB-syllabus Software Testing** (GOMYCODE) · **Software Engineer** and **REST API (Intermediate)** (HackerRank) · **Model Context Protocol** and **Claude Code in Action** (Anthropic) · **Data Science Essentials with Python** and **Linux Unhatched** (Cisco)
- Open to backend / full-stack roles — Tunis, Zaghouan or remote

---

## Tech Stack

**Backend &amp; Distributed Systems**

![Java](https://img.shields.io/badge/Java_21-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot_3-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![Apache Kafka](https://img.shields.io/badge/Apache_Kafka-231F20?style=for-the-badge&logo=apache-kafka&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![Keycloak](https://img.shields.io/badge/Keycloak-4D4D4D?style=for-the-badge&logo=keycloak&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)

**Databases**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Oracle](https://img.shields.io/badge/Oracle-F80000?style=for-the-badge&logo=oracle&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Hibernate](https://img.shields.io/badge/JPA_/_Hibernate-59666C?style=for-the-badge&logo=hibernate&logoColor=white)

**Languages**

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL_/_PL%2FSQL-CC2927?style=for-the-badge&logo=postgresql&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)

**Frontend**

![Angular](https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwind-css&logoColor=white)

**Testing, DevOps &amp; Observability**

![JUnit](https://img.shields.io/badge/JUnit5-25A162?style=for-the-badge&logo=junit5&logoColor=white)
![Testcontainers](https://img.shields.io/badge/Testcontainers-291A3F?style=for-the-badge&logo=docker&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

---

<h3 align="left">Connect with me</h3>
<p align="left">
  <a href="https://linkedin.com/in/achraf-rejouan" target="_blank">
    <img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="achraf-rejouan" height="30" width="40" />
  </a>
</p>

---

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Achraf-Rejouan/Achraf-Rejouan/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Achraf-Rejouan/Achraf-Rejouan/output/github-snake.svg" />
  <img alt="github-snake" src="https://raw.githubusercontent.com/Achraf-Rejouan/Achraf-Rejouan/output/github-snake.svg" />
</picture>
