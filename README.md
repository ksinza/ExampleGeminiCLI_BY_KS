# .NET Web API Scaffolder via Gemini CLI

This project provides a **smart template** to instantly generate a .NET Web API following **Clean Architecture** principles using the **Gemini CLI**. 

Instead of hosting the source code, this repository focuses on **AI-Driven Development**, providing the architectural "blueprint" (`gemini.md`) needed to scaffold a professional solution in seconds.

## 🏗️ Architecture Blueprint

The instructions within `gemini.md` are designed to generate a solution with high decoupling and SOLID principles:

* **Domain:** Core business entities (e.g., Products) and Repository interfaces.
* **Application:** Business logic, DTOs, and Service interfaces.
* **Infrastructure:** EF Core implementation, Data Context, and Persistence logic.
* **WebAPI:** ASP.NET Core Controllers and Dependency Injection.

### 📂 Expected Project Structure
When you run the generator, the AI will propose a solution organized like this:
```text
src/
├── SalesProject.Domain/         # Entities & Interfaces
├── SalesProject.Application/    # Business Logic & DTOs
├── SalesProject.Infrastructure/ # EF Core & DB Access
└── SalesProject.WebAPI/         # Controllers & Configuration
```
### .🤖 How to Generate the Project
This repository serves as a prompt-based generator. Follow these steps to create the project:

1. Prerequisites
Install the Gemini CLI.

Authenticate using your Google account: gemini auth login.

Have the .NET SDK installed.

2. Run the Generator
Clone this repo and run the following command in your terminal:

Bash
gemini ask --file gemini.md "Generate the complete .NET code following these clean architecture specifications"

### [!NOTE]
Language Note: The blueprint file gemini.md is written in Spanish. However, the Gemini CLI is capable of interpreting these instructions to generate high-quality code, comments, and project structures in English, following international coding standards.


🔥 Key Advantages
Flexibility: Unlike static templates, you can modify gemini.md to change entities or business rules, and the AI adapts the entire architecture.

Productivity: Reduces "Boilerplate Fatigue" by generating four layers and their dependencies in one go.

Modern C#: Instructions are optimized for .NET 8/9 features.


Developed by Kevin Sinza Salcedo Systems Engineer | 11+ years of experience in Software Development | .NET Specialist | Exploring AI-Driven Productivity.