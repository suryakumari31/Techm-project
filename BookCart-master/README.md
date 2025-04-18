# BookCart

BookCart is a full-stack e-commerce application for buying and selling books. It's built using .NET 8.0 for the backend and Angular 17 for the frontend.

## Features

### User Features
- User registration and authentication with JWT
- Password reset functionality via email
- Browse books by categories
- Search books by title or author
- Filter books by price range
- Add books to shopping cart
- Add books to wishlist
- Place orders
- View order history
- Responsive design for all devices

### Admin Features
- Secure admin panel
- Add new books
- Update existing books
- Delete books
- Manage book inventory
- View all orders

## Technical Stack

### Backend
- .NET 8.0
- Entity Framework Core
- MySQL Database
- JWT Authentication
- SMTP Email Service

### Frontend
- Angular 17
- Angular Material
- NgRx for state management
- RxJS
- SCSS for styling

## Getting Started

### Prerequisites
1. **Development Tools**
   - Visual Studio 2022 or VS Code
   - .NET 8.0 SDK (Download from [.NET Downloads](https://dotnet.microsoft.com/download))
   - Node.js v18+ (Download from [Node.js](https://nodejs.org/))
   - npm (comes with Node.js)
   - MySQL Server 8.0+ (Download from [MySQL](https://dev.mysql.com/downloads/mysql/))
   - Git (Download from [Git](https://git-scm.com/downloads))

2. **Required Extensions for VS Code**
   - C# Dev Kit
   - Angular Language Service
   - ESLint
   - Prettier
   - GitLens

### Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/BookCart.git
   cd BookCart
   ```

2. **Database Setup**
   ```bash
   # Create MySQL database
   mysql -u root -p
   CREATE DATABASE BookCartDB;
   exit;

   # Update connection string in appsettings.json
   {
     "ConnectionStrings": {
       "DefaultConnection": "Server=localhost;Database=BookCartDB;User=root;Password=yourpassword;"
     }
   }

   # Run database migrations
   dotnet ef database update
   ```

3. **Backend Setup**
   ```bash
   # Restore .NET packages
   dotnet restore

   # Build the project
   dotnet build
   ```

4. **Frontend Setup**
   ```bash
   # Navigate to ClientApp directory
   cd ClientApp

   # Install npm packages
   npm install

   # Install Angular CLI globally (if not already installed)
   npm install -g @angular/cli
   ```

5. **Environment Configuration**
   - Copy `appsettings.Development.json` to `appsettings.json`
   - Update the following settings:
     ```json
     {
       "ConnectionStrings": {
         "DefaultConnection": "your_connection_string"
       },
       "JWT": {
         "ValidAudience": "http://localhost:4200",
         "ValidIssuer": "http://localhost:5000",
         "Secret": "your_jwt_secret_key"
       },
       "EmailSettings": {
         "SmtpServer": "smtp.gmail.com",
         "SmtpPort": 587,
         "SmtpUsername": "your_email@gmail.com",
         "SmtpPassword": "your_app_password"
       }
     }
     ```

### Running the Application

1. **Start the Backend**
   ```bash
   # From the root directory
   dotnet run
   ```
   The API will be available at `https://localhost:7073`

2. **Start the Frontend**
   ```bash
   # From the ClientApp directory
   ng serve
   ```
   The application will be available at `http://localhost:4200`

### Default Admin Credentials
- Email: admin@bookcart.com
- Password: Admin@123

## Development Guidelines

### Code Style
- Follow Angular style guide for frontend code
- Use C# coding conventions for backend code
- Use meaningful variable and function names
- Add comments for complex logic
- Keep functions small and focused

### Git Workflow
1. Create a new branch for each feature
   ```bash
   git checkout -b feature/your-feature-name
   ```
2. Make your changes and commit
   ```bash
   git add .
   git commit -m "Description of your changes"
   ```
3. Push your changes
   ```bash
   git push origin feature/your-feature-name
   ```
4. Create a Pull Request

### Testing
- Run backend tests: `dotnet test`
- Run frontend tests: `ng test`
- Run e2e tests: `ng e2e`

## Troubleshooting

### Common Issues

1. **Database Connection Issues**
   - Verify MySQL service is running
   - Check connection string in appsettings.json
   - Ensure database exists and migrations are applied

2. **Frontend Build Issues**
   - Clear npm cache: `npm cache clean --force`
   - Delete node_modules: `rm -rf node_modules`
   - Reinstall packages: `npm install`

3. **JWT Authentication Issues**
   - Check JWT secret in appsettings.json
   - Verify token expiration settings
   - Ensure correct audience and issuer URLs

4. **Email Service Issues**
   - Verify SMTP settings
   - Check email credentials
   - Ensure proper network access

### Getting Help
- Check the [Issues](https://github.com/yourusername/BookCart/issues) page
- Create a new issue with:
  - Description of the problem
  - Steps to reproduce
  - Expected behavior
  - Actual behavior
  - Screenshots (if applicable)

## Project Structure

```
BookCart/
├── ClientApp/                 # Angular frontend
│   ├── src/
│   │   ├── app/
│   │   │   ├── components/   # Angular components
│   │   │   ├── services/     # Angular services
│   │   │   ├── state/        # NgRx state management
│   │   │   └── models/       # TypeScript interfaces
│   │   └── assets/           # Static assets
├── Controllers/              # API controllers
├── Models/                   # C# models
├── Services/                 # Business logic
├── DataAccess/              # Data access layer
└── Migrations/              # Database migrations
```

## Recent Updates

### UI/UX Improvements
- Converted category list to a dropdown menu for better space utilization
- Enhanced price filter component with a slider
- Improved responsive design for mobile devices
- Added loading states and error handling
- Enhanced form validation and error messages

### New Features
- Email-based password reset functionality
- Enhanced book filtering system
- Improved search functionality with autocomplete
- Better category management
- Enhanced shopping cart experience

### Technical Improvements
- Updated to .NET 8.0
- Migrated to Angular 17
- Improved state management with NgRx
- Enhanced security with JWT
- Better error handling and logging
- Optimized database queries
- Added comprehensive input validation

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Angular Material for UI components
- NgRx for state management
- Entity Framework Core for data access
- MySQL for database

## Contact

For any questions or support, please contact:
- Email:21a31a1218@pragati.ac.in
- GitHub: https://github.com/suryakumari31
