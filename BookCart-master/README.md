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
- .NET 8.0 SDK
- Node.js and npm
- MySQL Server
- Visual Studio 2022 or VS Code

### Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/BookCart.git
```

2. Set up the database
```bash
# Update the connection string in appsettings.json
# Run the following commands in Package Manager Console
Update-Database
```

3. Install frontend dependencies
```bash
cd ClientApp
npm install
```

4. Run the application
```bash
# From the root directory
dotnet run
```

The application will be available at `https://localhost:7073`

## Project Structure

```
BookCart/
├── ClientApp/                 # Angular frontend
│   ├── src/
│   │   ├── app/
│   │   │   ├── components/   # Angular components
│   │   │   │   ├── components/   # Angular components
│   │   │   │   ├── services/     # Angular services
│   │   │   │   ├── state/        # NgRx state management
│   │   │   │   └── models/       # TypeScript interfaces
│   │   │   └── assets/           # Static assets
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
