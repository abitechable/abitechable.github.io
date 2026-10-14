# IT Foundations & Career Pathways: A Practical Guide

**Audience:** Mixed — students, career-changers, early-career professionals  
**Goal:** Balance pathway comparison, actionable starting plans, and employability  
**Last Updated:** 2026-10-14

---

## Table of Contents

1. [Shared IT Foundations](#1-shared-it-foundations)
2. [Five Career Pathways](#2-five-career-pathways)
3. [Proof-of-Skill: Building a Verifiable Portfolio](#3-proof-of-skill-building-a-verifiable-portfolio)
4. [Employability: From Learning to Hiring](#4-employability-from-learning-to-hiring)
5. [Personal Development: The Long Game](#5-personal-development-the-long-game)
6. [Integrating Foundations into Experiments, Projects & Habits](#6-integrating-foundations-into-experiments-projects--habits)
7. [30-Day Starter Plans by Pathway](#7-30-day-starter-plans-by-pathway)
8. [Resources & Next Steps](#8-resources--next-steps)

---

## 1. Shared IT Foundations

*Every pathway builds on these. Spend 4–8 weeks here before specializing.*

| Foundation | Why It Matters | Minimum Viable Competency | How to Verify |
|------------|----------------|---------------------------|---------------|
| **Computer Systems** | Mental model for everything above | CPU/RAM/storage hierarchy, OS processes, file systems, boot sequence | Explain `top` output; trace a syscall |
| **Networking** | All distributed systems run on this | TCP/IP, DNS, HTTP/HTTPS, TLS, subnetting, ports, firewalls | Capture & analyze a curl request with `tcpdump`/`Wireshark` |
| **Linux/CLI** | Universal substrate | Navigation, permissions, `systemd`, logs, `ssh`, `grep`/`awk`/`sed`, package managers | Provision a VM, harden it, deploy a static site |
| **Scripting & Automation** | Force multiplier | Python or Bash: loops, functions, error handling, APIs, JSON/YAML | Automate a repetitive task end-to-end |
| **Version Control (Git)** | Collaboration & history | Branching, merging, rebasing, PR workflow, conventional commits | Contribute a PR to an open-source repo |
| **Databases (SQL)** | Data is the product | `SELECT`/`JOIN`/`GROUP BY`, indexes, transactions, normalization | Design & query a 3NF schema for a real domain |
| **Security Mindset** | Not optional | Threat modeling, least privilege, secrets management, OWASP Top 10 | Run `bandit`/`trivy` on your own code; fix findings |
| **Documentation & Communication** | Career accelerator | README-driven development, ADRs, runbooks, clear commit messages | Write a runbook a stranger could follow |

### Foundation Learning Loop (Repeat for Each)

```
1. Learn → 2. Do (lab) → 3. Teach (write/explain) → 4. Apply (project) → 5. Reflect (retro)
```

**Timebox:** 1 week per foundation, 2 hours/day. Use the **Feynman test**: if you can't explain it simply, you don't own it yet.

---

## 2. Five Career Pathways

*Choose one to go deep first. You can pivot later — foundations transfer.*

| Pathway | Core Question | Typical Titles | Primary Stack | Differentiator |
|---------|---------------|----------------|---------------|----------------|
| **Cloud & Platform Engineering** | How do we run reliable systems at scale? | Cloud Engineer, Platform Engineer, SRE, DevOps Engineer | AWS/Azure/GCP, Kubernetes, Terraform, Helm, ArgoCD, Observability | Infrastructure as product; developer experience focus |
| **Backend & Systems Engineering** | How do we build correct, performant services? | Backend Engineer, Systems Engineer, API Engineer | Go/Rust/Java/Node, PostgreSQL, Redis, gRPC, Kafka, SQL optimization | Data consistency, latency, throughput |
| **Data Engineering & Analytics** | How do we turn raw data into decisions? | Data Engineer, Analytics Engineer, ML Engineer | SQL, Python, Airflow/dbt, Spark/Flink, Iceberg/Delta, Warehouse (Snowflake/BigQuery) | Pipeline reliability, data quality, modeling |
| **Cybersecurity & Trust** | How do we protect assets and earn trust? | Security Engineer, AppSec, Cloud Sec, GRC, SOC Analyst | SIEM, CSPM, SAST/DAST, Threat Modeling, Zero Trust, Compliance frameworks | Risk reduction, incident response, assurance |
| **Full-Stack Product Engineering** | How do we ship usable features fast? | Full-Stack Engineer, Frontend Engineer, Product Engineer | React/Next.js, TypeScript, Tailwind, GraphQL/tRPC, Postgres, Vercel/AWS Amplify | End-to-end ownership, UX sense, shipping velocity |

### Pathway Comparison at a Glance

| Dimension | Cloud/Platform | Backend/Systems | Data Eng | Security | Full-Stack Product |
|-----------|----------------|-----------------|----------|----------|-------------------|
| **Daily Focus** | Infra, automation, reliability | Services, APIs, performance | Pipelines, models, quality | Threats, hardening, compliance | Features, UX, iteration speed |
| **Math/CS Depth** | Medium (distributed systems) | High (algorithms, concurrency) | High (stats, distributed compute) | Medium-High (crypto, protocols) | Medium (algorithms, UI state) |
| **Ops Exposure** | Very High | Medium | Medium | High | Low-Medium |
| **Cert Value** | High (AWS/Azure/GCP, CKAD) | Medium (architecture) | Medium (cloud, dbt) | **Very High** (CISSP, OSCP, cloud sec) | Low (portfolio > certs) |
| **Remote-Friendly** | ★★★★★ | ★★★★★ | ★★★★★ | ★★★★☆ | ★★★★★ |
| **Entry Barrier** | Medium | Medium-High | Medium | High (credential gatekeeping) | Low-Medium |
| **Salary Band (US, mid)** | $130–180k | $130–190k | $120–170k | $110–170k | $110–170k |

> **Rule:** Pick the pathway where the *daily work* energizes you, not just the salary. You'll spend 40+ hours/week doing it.

---

## 3. Proof-of-Skill: Building a Verifiable Portfolio

*Employers hire evidence, not claims. Every pathway needs the same proof structure.*

### The Portfolio Formula

```
Portfolio = Σ (Project × Context × Artifact × Reflection)
```

| Component | What It Is | Minimum Bar |
|-----------|------------|-------------|
| **Project** | Real problem, scoped, finished | 3–5 substantial projects per pathway |
| **Context** | Why this problem? Constraints? Trade-offs? | One-pager per project: problem, constraints, decisions, outcomes |
| **Artifact** | Code, infra, docs, diagrams, tests | Public repo + live demo (where applicable) + Architecture Decision Records |
| **Reflection** | What you'd do differently | Retro note: failures, surprises, next steps |

### Pathway-Specific Portfolio Projects

| Pathway | Project 1 (Foundation) | Project 2 (Core) | Project 3 (Advanced) | Project 4 (Specialization) |
|---------|------------------------|------------------|----------------------|----------------------------|
| **Cloud/Platform** | Terraform: VPC + EC2 + RDS | EKS/GKE cluster + ArgoCD + monitoring | Multi-env platform (dev/staging/prod) with self-service API | Custom operator / provider / policy engine |
| **Backend/Systems** | REST API + Postgres + tests | gRPC service + Redis cache + rate limiting | Distributed system: leader election / consensus / sharding | High-throughput ingest / real-time streaming |
| **Data Engineering** | ELT pipeline: API → S3 → Snowflake | dbt models + tests + CI + documentation | Streaming pipeline: Kafka → Flink → Iceberg | ML feature store / real-time analytics dashboard |
| **Security** | Harden a Linux server + audit | Threat model + mitigations for a web app | CI/CD pipeline with SAST/DAST/SCA + policy as code | Incident response simulation / purple team exercise |
| **Full-Stack Product** | CRUD app + auth + deploy | Real-time collab feature (WebSockets/CRDT) | Design system + component library + Storybook | End-to-end product: billing, analytics, admin panel |

### Artifact Standards (Non-Negotiable)

- **README**: Problem, architecture diagram, run instructions, trade-offs
- **CI/CD**: Lint, test, build, deploy on every push
- **Tests**: Unit + integration + contract (where applicable)
- **Observability**: Logs, metrics, traces in the project itself
- **Security**: No secrets in repo; `trivy`/`bandit` clean
- **License**: MIT or Apache-2.0 (unless otherwise required)

---

## 4. Employability: From Learning to Hiring

### The Hiring Funnel Reality

```
Applications → Screen → Technical → Behavioral → Offer
   100           20         8           4          1
```

**Optimize for conversion at each stage, not volume.**

### Stage-by-Stage Tactics

| Stage | What They Evaluate | Your Leverage |
|-------|-------------------|---------------|
| **Application** | Keywords, trajectory, projects | Tailored resume (1 page); portfolio links; referral |
| **Screen (15–30 min)** | Communication, baseline fit | STAR stories; "I don't know, but here's how I'd find out" |
| **Technical** | Problem-solving, code quality, systems thinking | Think aloud; clarify constraints; write clean code; trade-off discussion |
| **Behavioral** | Collaboration, ownership, growth | Specific examples: conflict, failure, mentorship, ambiguity |
| **Offer** | Value alignment, negotiation | Know market data; negotiate total comp (equity, sign-on, PTO, growth budget) |

### Resume Patterns That Work

```
[Role] @ [Company] | [Dates]
• [Action verb] [Scope] [Technology] → [Quantified outcome]
• Example: "Designed and deployed multi-region Kafka cluster (3 AZs, 50TB/day) reducing p99 latency 40% and cutting infra cost $18k/mo"
```

**One-liner per bullet. Lead with impact. Numbers > adjectives.**

### Networking Without "Networking"

1. **Learn in public**: Weekly 200-word post on what you built/learned (LinkedIn, Dev.to, X)
2. **Answer questions**: Stack Overflow, Discord, Reddit — build reputation
3. **Cold DM with specificity**: "Saw your post on [topic]. I built [project] solving similar. Mind if I share a 2-min Loom?"
4. **Referrals come from competence visibility**, not coffee chats

---

## 5. Personal Development: The Long Game

*Technical skills decay. Meta-skills compound.*

### The 4-Pillar Personal OS

| Pillar | Practice | Frequency | Metric |
|--------|----------|-----------|--------|
| **Deliberate Learning** | 1 deep-dive/week (paper, source code, RFC) | Weekly | Can explain to peer |
| **Health & Energy** | Sleep 7.5h, zone-2 cardio 3×/wk, resistance 2×/wk | Daily | HRV, subjective energy |
| **Relationship Capital** | 1 meaningful conversation/week (mentor, peer, junior) | Weekly | Network graph density |
| **Strategic Reflection** | Monthly retro: what worked, what didn't, next 30 days | Monthly | Decision quality trend |

### Career Compass Questions (Quarterly)

1. What problems do I enjoy solving *even when they're hard*?
2. Which skills am I building that will be valuable in 5 years?
3. Who are the 3 people I learn most from? Am I staying in touch?
4. What's my "optionality fund" (savings + skills) for a pivot?
5. Am I saying "no" to good opportunities to leave room for great ones?

### Avoiding Burnout Traps

| Trap | Antidote |
|------|----------|
| Tutorial hell | Build → break → fix → teach (no passive consumption) |
| Imposter syndrome | Track wins weekly; compare to 6 months ago, not experts |
| Shiny object chasing | Commit to one pathway for 6 months; log "parking lot" ideas |
| Isolation | Pair program weekly; join a learning cohort; mentor someone |

---

## 6. Integrating Foundations into Experiments, Projects & Habits

*Don't learn foundations in isolation. Fold them into pathway work immediately.*

### The Integration Matrix

| Foundation | Cloud/Platform Experiment | Backend Experiment | Data Eng Experiment | Security Experiment | Full-Stack Experiment |
|------------|---------------------------|-------------------|---------------------|---------------------|----------------------|
| **Systems** | `stress-ng` on EC2; compare cgroups vs namespaces | Profile Go/Rust service with `pprof`/`perf` | Memory-profile Spark executor | Analyze `/proc` for anomaly detection | Profile Node.js event loop lag |
| **Networking** | VPC flow logs → Athena queries | `tcpdump` API latency; simulate packet loss | Capture Kafka broker traffic | MITM proxy for API inspection | Service worker offline-first |
| **Linux/CLI** | `systemd` unit for custom daemon | `strace` syscall analysis | Cron → systemd timers for pipelines | `auditd` rules for file integrity | `ssh` config for multi-host deploy |
| **Scripting** | Python: Terraform plan parser | Bash: zero-downtime deploy script | Python: Great Expectations data quality | Python: cert expiry scanner | Node: PR preview deploy script |
| **Git** | Monorepo: Terraform + Helm + apps | Trunk-based dev + feature flags | dbt project: models as code | Policy-as-code repo with PR gates | Design system: versioned components |
| **SQL** | RDS Performance Insights query analysis | `EXPLAIN ANALYZE` on slow queries | dbt incremental models + partitioning | Query audit logs for anomalies | Postgres full-text search + RLS |
| **Security** | IAM least-privilege policies | mTLS between services | Column-level encryption + key rotation | Threat model → mitigations → tests | CSP headers + COOP/COEP |
| **Docs/Comm** | Runbook: "EKS node stuck in NotReady" | ADR: "Why gRPC over REST" | Data dictionary + lineage graph | Incident postmortem template | Component README + visual tests |

### Professional Habits (Start Day 1)

| Habit | Trigger | Action | Time |
|-------|---------|--------|------|
| **Daily Log** | End of day | 3 bullets: done, blocked, tomorrow | 5 min |
| **Weekly Retro** | Friday 4pm | What worked? What didn't? One improvement | 30 min |
| **Learning Sprint** | Monday AM | Pick one concept; build micro-project by Friday | 2–4 hrs/wk |
| **Code Review** | Every PR | Review others; ask for review on yours | Continuous |
| **Public Artifact** | Monthly | Publish one: blog, tool, talk, diagram | 2–4 hrs/mo |
| **Health Check** | Quarterly | Run compass questions; adjust plan | 1 hr |

---

## 7. 30-Day Starter Plans by Pathway

*Each assumes foundations are in progress (Week 1–2 overlap).*

### Cloud & Platform Engineering

| Week | Focus | Deliverable |
|------|-------|-------------|
| 1 | AWS/GCP/Azure free tier: VPC, subnets, IGW, NAT | Terraform: deploy 3-tier VPC (public/private/data) |
| 2 | Compute: EC2/VM → ASG → ALB | Terraform: auto-scaling group with health checks |
| 3 | Containers: Docker → ECR/Artifact Registry → ECS/Fargate | Deploy containerized API with blue/green |
| 4 | K8s: Kind → EKS/GKE → Helm → ArgoCD | GitOps-deployed cluster with monitoring (Prom/Grafana) |

### Backend & Systems Engineering

| Week | Focus | Deliverable |
|------|-------|-------------|
| 1 | Go/Rust basics: HTTP server, JSON, tests | REST API: CRUD + SQLite + integration tests |
| 2 | Postgres: schema, indexes, transactions, migrations | Migrate to Postgres; add connection pooling |
| 3 | Concurrency: workers, channels, rate limiting | Async job processor with retries + dead-letter |
| 4 | Observability: structured logs, metrics, traces | OpenTelemetry-instrumented service + Grafana dashboards |

### Data Engineering

| Week | Focus | Deliverable |
|------|-------|-------------|
| 1 | SQL mastery: CTEs, window functions, `EXPLAIN` | Analytics queries on public dataset (e.g., TPC-H) |
| 2 | Python + pandas → dbt project | dbt models: staging → intermediate → marts + tests |
| 3 | Orchestration: Airflow or Dagster | DAG: extract API → load S3 → transform dbt → validate |
| 4 | Streaming: Kafka → Flink/Spark Structured Streaming | Real-time pipeline: CDC → Kafka → Iceberg table |

### Cybersecurity

| Week | Focus | Deliverable |
|------|-------|-------------|
| 1 | Linux hardening: CIS benchmarks, `auditd`, `fail2ban` | Hardened VM + audit report |
| 2 | AppSec: OWASP Top 10, SAST/DAST, dependency scanning | Secure code review + CI pipeline with `trivy`/`semgrep` |
| 3 | Cloud security: IAM analysis, CSPM, CloudTrail | Terraform: least-privilege roles + drift detection |
| 4 | Incident response: tabletop, log analysis, forensics | Runbook + simulated incident with timeline |

### Full-Stack Product Engineering

| Week | Focus | Deliverable |
|------|-------|-------------|
| 1 | React + TypeScript + Vite + Tailwind | Component library: Button, Input, Card + Storybook |
| 2 | Next.js: App Router, Server Components, Auth (NextAuth) | Deployed app: auth + protected routes + DB (Vercel + Neon) |
| 3 | Real-time: WebSockets / tRPC / Server-Sent Events | Collaborative feature (whiteboard / presence / chat) |
| 4 | Product polish: analytics, error tracking, feature flags | Launch-ready: PostHog, Sentry, LaunchDarkly, Stripe billing |

---

## 8. Resources & Next Steps

### Curated Learning Sources (High Signal, Low Noise)

| Type | Recommendations |
|------|-----------------|
| **Systems/Networking** | *Computer Systems: A Programmer's Perspective* (CSAPP); *Beej's Guide to Network Programming*; `brendangregg.com` |
| **Linux/CLI** | *The Linux Command Line* (Shotts); `linuxjourney.com`; *How Linux Works* (Ward) |
| **Cloud** | Cloud provider *Well-Architected Framework* docs; *Terraform Up & Running* (Brikman); *Kubernetes the Hard Way* (Kelsey Hightower) |
| **Backend** | *Designing Data-Intensive Applications* (Kleppmann); *Go by Example*; *Effective Go* |
| **Data** | *Fundamentals of Data Engineering* (Reis/Housley); *dbt Learn*; *Designing Event-Driven Systems* (Ben Stopford) |
| **Security** | *OWASP Cheat Sheets*; *Practical Malware Analysis*; *Cloud Security Handbook* (O'Reilly); *Blue Team Handbook* |
| **Full-Stack** | *React Official Tutorial*; *TypeScript Handbook*; *Next.js Learn*; *Kent C. Dodds' Epic React* |

### Practice Platforms

| Platform | Best For |
|----------|----------|
| **LeetCode / Codeforces** | Algo interview prep (Backend, Data) |
| **Hack The Box / TryHackMe** | Security hands-on |
| **Cloud Sandboxes** (AWS Skill Builder, Azure Learn, GCP Qwiklabs) | Cloud labs |
| **Kaggle / DataTalks.Club** | Data projects |
| **Frontend Mentor / CodePen** | UI implementation practice |

### Communities Worth Joining

- **Cloud/Platform:** CNCF Slack, Platform Engineering Slack, r/platformengineering
- **Backend:** r/golang, r/rust, Systems Design Discord
- **Data:** dbt Slack, Data Engineering Weekly, Locally Optimistic
- **Security:** DEF CON groups, OWASP chapters, r/netsec
- **Full-Stack:** Reactiflux, Next.js Discord, IndieHackers

### Immediate Next Actions (Today)

1. **Pick your pathway** — use the comparison table; commit to 6 months
2. **Start Foundation Week 1** — Linux + Networking (highest transfer)
3. **Create GitHub repo** — `learning-journal` — daily 3-bullet log
4. **Schedule weekly retro** — Friday 4pm calendar invite (recurring)
5. **Find one accountability partner** — peer at similar stage; 30-min weekly sync

---

## Appendix: Pathway Decision Flowchart

```
START
  │
  ├─ Do you love infra, automation, "how does this run?" → CLOUD/PLATFORM
  │
  ├─ Do you love algorithms, latency, correctness, "how does this scale?" → BACKEND/SYSTEMS
  │
  ├─ Do you love SQL, pipelines, modeling, "what does this data mean?" → DATA ENGINEERING
  │
  ├─ Do you love breaking things, threat models, "how do we protect this?" → SECURITY
  │
  └─ Do you love UX, shipping features, "how do users experience this?" → FULL-STACK PRODUCT
```

> **Final reminder:** The best pathway is the one you'll stick with long enough to get good. Foundations make switching possible. Depth makes you hireable. Consistency makes you senior.

---

*Document version 1.0 — iterate as you learn. Share with peers. Improve together.*