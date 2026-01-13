# ReportMitra – Automation & CI/CD Repository

## 📌 Overview

This repository contains **all CI/CD pipelines and infrastructure automation workflows** used to deploy, manage, and optimize the **ReportMitra ecosystem**, including:

- 🌐 Citizen-facing platform (`reportmitra.in`)
- 🛠️ Admin portal (`admin.reportmitra.in`)
- ⚙️ Backend APIs (Django REST Framework)
- 🚀 Frontend applications (Vite + React)
- ☁️ AWS infrastructure lifecycle automation
- ⏱️ Cost-optimized start/stop scheduling

The primary goal of this repository is to **fully automate deployments, reduce operational overhead, and enforce consistent infrastructure practices** across environments.

---

## 🏗️ What This Repository Automates

### 1. Application Deployment
- Backend API deployment to EC2
- Citizen frontend deployment to S3 + CloudFront
- Admin frontend deployment to S3 + CloudFront

### 2. Infrastructure Lifecycle
- Automated start/stop of EC2 instances
- Manual override workflows for infrastructure control
- Cron-based cost optimization

### 3. CI/CD Pipelines
- Git-based triggers (on `main` branch)
- Environment-safe deployments
- Zero-downtime update strategy

---

## 📁 Repository Structure

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
