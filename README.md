# Student Management System - ASP.NET Core Web API


This project is a Student Management System developed using **ASP.NET Core Web API** following **Layered Architecture** principles. It provides secure REST APIs for managing student records with SQL Server as the database.

---

# Features

- Get All Students
- Get Student by Id
- Add Student
- Update Student
- Delete Student
- Layered Architecture
- Entity Framework Core
- SQL Server
- Swagger API Documentation
- JWT Authentication
- Global Exception Handling Middleware
- Serilog Logging

---

# Technology Stack

- ASP.NET Core Web API (.NET 10)
- C#
- Entity Framework Core
- SQL Server
- Swagger (Swashbuckle)
- JWT Authentication
- Serilog

---

# Project Structure

```
StudentManagement.API
│
├── Controllers
├── Middleware
├── Program.cs
├── appsettings.json
│
StudentManagement.Domain
│
├── Models
│
StudentManagement.Data
│
├── Context
├── Migrations
│
StudentManagement.Repository
│
├── Interfaces
└── Implementations
│
StudentManagement.Service
│
├── Interfaces
└── Implementations
```

---

# Database

Database Name

```
StudentManagementDB
```

Student Table

| Column | Type |
|---------|------|
| Id | int (Identity) |
| Name | nvarchar |
| Email | nvarchar |
| Age | int |
| Course | nvarchar |
| CreatedDate | datetime |

---

# API Endpoints

## Get All Students

```
GET /api/Student
```

---

## Get Student By Id

```
GET /api/Student/{id}
```

---

## Add Student

```
POST /api/Student
```

Request Body

```json
{
  "name": "Nikita",
  "email": "nikita@gmail.com",
  "age": 25,
  "course": "Full Stack"
}
```

---

## Update Student

```
PUT /api/Student/{id}
```

Request Body

```json
{
  "id": 1,
  "name": "Nikita",
  "email": "nikita@gmail.com",
  "age": 26,
  "course": "ASP.NET Core"
}
```

---

## Delete Student

```
DELETE /api/Student/{id}
```

---

# Setup Instructions

## Clone Repository

```bash
git clone <repository-url>
```

---

## Open Project

Open the solution in **Visual Studio 2022**.

---

## Restore Packages

```
Build → Restore NuGet Packages
```

or

```bash
dotnet restore
```

---

## Update Database Connection

Open

```
appsettings.json
```

Update the SQL Server connection string.

Example

```json
"ConnectionStrings": {
  "DefaultConnection": "Server=(localdb)\\MSSQLLocalDB;Database=StudentManagementDB;Trusted_Connection=True;TrustServerCertificate=True;"
}
```

---

## Apply Migration

Open Package Manager Console

```powershell
Update-Database
```

---

## Run Project

Press

```
F5
```

or

```bash
dotnet run
```

---

## Swagger

Open

```
https://localhost:<port>/swagger
```

---

# Architecture

```
Controller
      │
      ▼
Service
      │
      ▼
Repository
      │
      ▼
Entity Framework Core
      │
      ▼
SQL Server
```

---

# Exception Handling

- Global Exception Middleware
- Proper HTTP Status Codes
- Meaningful Error Messages

---

# Logging

- Serilog
- Console Logging
- File Logging

---

# Security

- JWT Authentication
- Protected API Endpoints
- Authorization Support

---


