# ReportMitra – DevOps Automation & CI/CD Orchestration Repository

## 📖 Introduction

This repository serves as the **central automation and orchestration layer** for the entire **ReportMitra platform**, covering both:

- 🌍 **Citizen-facing application** (`reportmitra.in`)
- 🛠️ **Administrative platform** (`admin.reportmitra.in`)

It encapsulates **all CI/CD pipelines, infrastructure lifecycle workflows, and operational automations** required to reliably deploy, manage, and optimize the system in a production AWS environment.

This repository intentionally contains **no application business logic**.  
Instead, it focuses purely on **deployment, infrastructure control, and operational reliability**.

---

## 🎯 Objectives of This Repository

The design of this repository is guided by the following objectives:

1. **Full Automation**
   - No manual SSH-based deployments
   - No manual frontend uploads
   - No manual server start/stop for routine operations

2. **Separation of Concerns**
   - Citizen and Admin systems are deployed independently
   - Frontend and backend lifecycles are decoupled
   - Infrastructure control is isolated from application deployment

3. **Operational Safety**
   - Role separation between admin and citizen services
   - Minimal blast radius for failures
   - Manual override pipelines for emergencies

4. **Cost Optimization**
   - Infrastructure is not kept running unnecessarily
   - Time-based automation aligns with real operational usage

5. **Scalability & Maintainability**
   - Easy onboarding for new engineers
   - Predictable deployment behavior
   - Extendable pipelines

---

## 🧱 Platform Architecture Context

The ReportMitra ecosystem consists of:

### Backend
- Django REST Framework
- Single unified MySQL database (Amazon RDS)
- Hosted on Amazon EC2
- Shared by both admin and citizen applications

### Frontend
- Vite + React (JavaScript)
- Tailwind CSS
- Static asset hosting on Amazon S3
- Distributed via Amazon CloudFront

This repository **does not provision infrastructure**, but **controls and operates it** once provisioned.

---

## 📁 Repository Structure & Responsibility

```text
.
├── backend-deploy.yml
├── frontend-deploy.yml
├── admin-backend-deploy.yml
├── admin-frontend-deploy.yml
├── infra-start.yml
├── infra-stop.yml
├── infra-start-manual.yml
├── infra-stop-manual.yml
└── README.md
