# BookCart - Online Book Store Platform

## 🚀 Technology Stack
- **Backend**: ASP.NET Core 8 Web API
  - Entity Framework Core (MySQL provider)
  - JWT Authentication
  - Swagger/OpenAPI documentation
  - Repository pattern implementation
- **Frontend**: Angular 18
  - Angular Material UI
  - Standalone components
  - Lazy loading
  - Reactive forms
- **Database**: MySQL (configured in appsettings.json)

## 📋 Prerequisites
- **Development Tools**:
  - Visual Studio 2022 or VS Code
  - .NET 8 SDK
  - Node.js v18+
  - Angular CLI v18+
- **Database**:
  - MySQL Server 8.0+
  - MySQL Workbench (recommended)

## 🛠️ Project Structure
```
BookCart-master/
├── BookCart/               # .NET Backend
│   ├── Controllers/        # API endpoints
│   ├── DataAccess/         # Repository layer
│   ├── Models/             # Database models
│   ├── Migrations/         # EF Core migrations
│   └── Program.cs          # Startup configuration
├── ClientApp/              # Angular Frontend
│   ├── src/
│   │   ├── app/            # Angular components
│   │   ├── assets/         # Static files
│   │   └── environments/   # Configuration
└── DBScript/               # Database schema
```

## ⚙️ Setup Instructions

### 1. Database Configuration
1. Create MySQL database:
```sql
CREATE DATABASE BookCartDB;
```
2. Run initial migration:
```bash
dotnet ef database update
```

### 2. Backend Setup
1. Update connection string in `appsettings.json`:
```json
"ConnectionStrings": {
  "DefaultConnection": "Server=localhost;Database=BookCartDB;User=root;Password=yourpassword;"
}
```
2. Install dependencies:
```bash
dotnet restore
```

### 3. Frontend Setup
1. Navigate to ClientApp:
```bash
cd BookCart/ClientApp
```
2. Install packages:
```bash
npm install
```

## 🏃 Running the Application
1. Start backend:
```bash
dotnet run
```
2. In separate terminal, start frontend:
```bash
cd ClientApp
ng serve
```
3. Access application at: `http://localhost:4200`

## 🔍 API Documentation
Swagger UI available at: `http://localhost:5000/swagger`

## 📜 License
MIT License - Copyright © 2024 Surya Kumari Mukka. See [LICENSE](LICENSE) for full details.

## ✉️ Contact
Maintained by Surya Kumari Mukka  
Email:suryakumarimukka333@gmail.com
