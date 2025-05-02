# KampusCU - Campus Management System

## 📁 Overview

**KampusCU** is a comprehensive campus management system built with **ASP.NET Core 6.0**. It enables universities to efficiently manage departments, classes, clubs, events, and announcements through a modern API-based architecture.

---

## 🏠 Technologies & Architecture

### 🔹 Core Architecture

* **Clean/Onion Architecture**
* **CQRS Pattern** with MediatR
* **Repository Pattern** for data abstraction
* **DTOs** for communication between layers

### 🔹 Backend Technologies

* ASP.NET Core 6.0
* Entity Framework Core 6.0
* SQL Server
* AutoMapper
* Swagger / OpenAPI
* JWT Authentication
* API Versioning
* Serilog (with database sinks)

### 🔹 Infrastructure Components

* Hangfire (background jobs)
* File Storage Services
* Custom Exception Middleware
* Automated Database Backup System

---

## ⚙️ CI/CD & Deployment

### 🚀 GitHub Actions Workflow

* Triggered on push and PR to `master`
* **Stages**:

  * Build & Test (restore, build, test)
  * Docker Build & Push (multi-stage build, DockerHub push)
  * Deploy via SSH (Docker Compose, auto-restart)
* Uses repository secrets for credentials and keys

### 💪 Dockerization

* Multi-stage Docker build
* Docker Compose orchestration
* Nginx reverse proxy in production
* Images hosted on Docker Hub

---

## 🔐 Security

### 🔑 JWT Authentication

* Full API protection
* Access & Refresh token support
* Stateless, secure API sessions

### ⛓️ Password Hashing

* HMACSHA512-based hashing with salt
* Secure verification logic
* Resistant to brute-force attacks

### ✨ Encryption

* Custom encryption logic for sensitive operations

---

## 📄 Project Structure

```text
KampusCU/
├── Core/
│   ├── Domain/          # Entities and business objects
│   └── Application/     # Business logic, DTOs, interfaces
│
├── Infrastructure/
│   ├── Core/            # Cross-cutting concerns
│   ├── Infrastructure/  # Implementation of application interfaces
│   └── Persistence/     # Data access, EF Core, repositories
│
├── Presentation/
│   └── API/             # ASP.NET Core Web API
│
└── Docker, CI/CD files, etc.
```

---

## 🚀 Features

* Role-based User Management (Admin, Student)
* Department & Class Management
* Club & Event Management
* Campus-wide Announcements
* File Upload & Download
* Automated Backups

---

## 👨‍💼 Development Team

Graduation project by **Mücahit** & **Şeyma**
