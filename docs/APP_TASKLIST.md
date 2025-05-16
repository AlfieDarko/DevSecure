# DevSecOps Security Scanner – Execution Plan

This is a structured development checklist to guide the MVP build. Each phase focuses on delivering functional chunks that move the project forward rapidly.

---

## ✅ Phase 1: Foundation (Week 1–3)

**High Priority – Core App Setup**
- [ ] Repo structure & monorepo bootstrapping
- [ ] Rust API skeleton + auth/token endpoints
- [ ] PostgreSQL schema: users, projects, scans
- [ ] React TS dashboard skeleton with auth
- [ ] Redis setup for token/session caching
- [ ] RabbitMQ setup and test Rust producer/consumer
- [ ] GitHub webhook endpoint + test delivery

---

## 🔍 Phase 2: Infrastructure Scanning MVP (Week 2–3)

**Accelerated using tools like `tfsec`, `checkov`**
- [ ] Integrate `tfsec` CLI as async scanner
- [ ] Parse output to JSON → insert into DB
- [ ] Display scan result summary in dashboard
- [ ] S3 upload for full reports
- [ ] Signed URL fetch from frontend
- [ ] Auto-rescan on new commit via webhook

---

## ⚙️ Phase 3: CI/CD + Container Security (Week 4–6)

**Use `trivy`, `grype`, or `dockle`**
- [ ] GitHub Action template for PR scans
- [ ] CI policy enforcement (fail builds w/ critical issues)
- [ ] Integrate `trivy` for image scans
- [ ] Parse and store vuln findings
- [ ] Show container scan results in dashboard
- [ ] Policy config in UI (e.g. block criticals)

---

## 📊 Phase 4: Reporting + Compliance (Week 6–8)

- [ ] Compliance mapping dashboard (e.g. Cyber Essentials % complete)
- [ ] PDF report generation (use HTML template + headless Chromium or WeasyPrint)
- [ ] Report upload to S3
- [ ] Show compliance status by project
- [ ] Trend chart: risk scores over time

---

## 🔐 Security & Observability Hardening

- [ ] Role-based access control
- [ ] Input sanitization, validation middleware
- [ ] Prometheus metrics for API + job queue
- [ ] ELK or Loki for logging
- [ ] Alerts on failed scans or high vulns

---

## 🧪 Test & Deploy

- [ ] Seed data for demo
- [ ] Dockerize backend/frontend
- [ ] Terraform + K8s deploy
- [ ] CI pipeline: test, build, deploy
- [ ] Optional: deploy demo site

---
