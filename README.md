# 🏦 Online Banking System (Web API + Angular)

This is a full-stack **Online Banking System** application with a **.NET Core Web API backend** and an **Angular frontend** which follows pure code first approach. The backend provides RESTful API endpoints for all banking operations, while the frontend offers a clean user interface for customers and admins.

The APIs are documented and testable via **Swagger UI**, and the frontend is built with **Angular CLI** to consume these endpoints.

---

## 📌 Key Features (Modules)

This project contains 6 main modules:

### 🔐 1. Login & Registration
User authentication and account creation.

### 🛠️ 2. Admin
Admin can manage customers, view system-wide activity, and control core operations.

### 🏦 3. Open an Account
Users can open new account.

### 💸 4. Fund Transfer
Transfer funds between accounts securely.

### 👥 5. Add Beneficiary
Add and manage beneficiaries for transferring funds.

### 📊 6. Dashboard
Get account summary, account statement, and transaction history in a centralized view.

---

## 🛠 Technologies Used

- **Backend:** .NET Core Web API  
- **Frontend:** Angular 15+  
- **API Testing & Docs:** Swagger UI
- **Database:** SQL Server  
- **IDE:** Visual Studio, VS Code  
- **ORM:** Entity Framework Core

---

## 🧰 Tools Required

- [Visual Studio 2019/2022](https://visualstudio.microsoft.com/)  
- [SQL Server & SSMS](https://learn.microsoft.com/sql/ssms/download-sql-server-management-studio-ssms)  
- [.NET SDK 6.0+](https://dotnet.microsoft.com/en-us/download)  
- [Node.js (v16+)](https://nodejs.org/)  
- [Angular CLI](https://angular.io/cli)  

---

## 📂 Project Structure

```
Root/
├── OnlineBanking/              # Backend (.NET Core Web API)
│   ├── Controllers/
│   ├── Models/
│   ├── Data/
│   ├── Startup.cs
│   └── appsettings.json
│
├── OnlineBanking-Frontend/     # Frontend (Angular)
│   ├── src/
│   ├── angular.json
│   └── package.json
└── OnlineBanking.sln           # Solution file
```

---

## 🚀 How to Run the Project

### ✅ Prerequisites

- .NET SDK 6.0+  
- SQL Server & SSMS  
- Node.js v16+  
- Angular CLI installed globally:
  ```bash
  npm install -g @angular/cli
  ```

---

### 🔧 Backend (.NET Core API)

1. **Open the Solution**
   - Open `OnlineBanking.sln` in Visual Studio.

2. **Configure the Connection String**
   - Open `appsettings.json`:
     ```json
     "ConnectionStrings": {
       "DefaultConnection": "Server=YOUR_SERVER;Database=OnlineBankingDB;Trusted_Connection=True;"
     }
     ```

3. **Run EF Migrations (if needed)**
   ```bash
   dotnet ef database update
   ```

4. **Run the Backend**
   - Press `F5` or `Ctrl + F5` in Visual Studio.
   - Swagger should open at:  
     ```
     https://localhost:xxxx/swagger
     ```

---

### 🌐 Frontend (Angular)

1. **Navigate to the frontend folder**
   ```bash
   cd OnlineBanking-Frontend
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Run the Angular app**
   ```bash
   ng serve
   ```

4. **Access the App**
   - Open your browser and go to:  
     ```
     http://localhost:4200
     ```

   > ✅ Ensure that the backend is running at the expected `https://localhost:xxxx` port.

---

## 🧪 Testing the API with Swagger

- Visit:  
  ```
  https://localhost:xxxx/swagger
  ```
- You can:
  - View and test all API endpoints
  - Check response formats
  - See HTTP status codes

---

## 📌 Best Practices

- Use `DTOs` for secure and efficient data transfer  
- Validate requests using `[DataAnnotations]`  
- Use `async/await` for scalability  
- Secure endpoints with role-based authorization *(if applicable)*  
- Use Angular `services` to manage API requests

