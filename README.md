# E-commerce Application

A full-stack e-commerce application with Spring Boot backend and React frontend.

## Features

### Backend
- Complete product management with CRUD operations
- Image upload and retrieval for products
- Flexible search functionality across multiple fields (name, description, brand, category)
- RESTful API endpoints with proper HTTP status code handling
- Cross-Origin Resource Sharing (CORS) enabled for frontend integration
- PostgreSQL integration for data persistence

### Frontend
- Responsive product catalog with React
- Product search functionality
- Shopping cart management with local storage persistence
- Checkout process
- Light/Dark theme toggle
- Category filtering
- Admin features for product management (add, update, delete)

## Technology Stack

### Backend
- Java 21
- Spring Boot 3.4.3
- Spring Data JPA
- PostgreSQL
- Maven

### Frontend
- React 18
- React Router v6
- Axios for API calls
- Bootstrap 5 for UI
- Context API for state management
- Vite as build tool

## API Endpoints

| Method | URL                      | Description                              |
|--------|--------------------------|------------------------------------------|
| GET    | /api/products            | Get all products                         |
| GET    | /api/product/{id}        | Get product by ID                        |
| GET    | /api/product/{id}/image  | Get product image by product ID          |
| POST   | /api/product             | Add a new product                        |
| PUT    | /api/product/{id}        | Update an existing product               |
| DELETE | /api/product/{id}        | Delete a product                         |
| GET    | /api/products/search     | Search products by keyword               |

## Setup and Installation

### Prerequisites
- Java 21
- PostgreSQL
- Maven
- Node.js and npm

# Database connection settings
spring.datasource.url=jdbc:postgresql://localhost:5432/ecommerce_db
spring.datasource.username=postgres
spring.datasource.password=your_password_here
spring.datasource.driver-class-name=org.postgresql.Driver

# JPA/Hibernate settings
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

Note: Replace the placeholder values with your actual database configuration.
The application uses JPA with ddl-auto=update, so tables will be created automatically.

2. Build and run the Spring Boot application:
```bash
cd backend/SpringEcom
./mvnw clean install
./mvnw spring-boot:run
```

The backend will start on http://localhost:8080

### Frontend Setup
1. Install dependencies:
```bash
cd frontend/ecom-frontend-5
npm install
```

2. Run the development server:
```bash
npm run dev
```

The frontend will start on http://localhost:5173

### Integration
The frontend is already configured to connect to the backend API:
- API base URL is set to `http://localhost:8080/api` in the Axios configuration
- CORS is enabled on the backend via the `@CrossOrigin` annotation in the controllers
- All product endpoints support JSON format
- Product creation and updates use `multipart/form-data` for image handling



## Project Structure

```
├── backend/SpringEcom/
│   ├── src/main/java/com/telusko/SpringEcom/
│   │   ├── controller/        # REST controllers
│   │   ├── model/             # Entity classes
│   │   ├── repo/              # Repository interfaces
│   │   ├── service/           # Business logic
│   │   └── SpringEcomApplication.java  # Main application class
│   ├── src/main/resources/    # Application properties and configurations
│   └── pom.xml                # Maven dependencies
│
└── frontend/ecom-frontend-5/
    ├── public/                # Static assets
    ├── src/
    │   ├── components/        # React components
    │   ├── Context/           # Application state management
    │   ├── assets/            # Images and other resources
    │   ├── App.jsx            # Main application component
    │   └── main.jsx           # Application entry point
    ├── package.json           # npm dependencies
    └── vite.config.js         # Vite configuration
```

## Application Features

### Product Management
- View all products with images, descriptions, and prices
- Filter products by category
- Search products by name, description, brand, or category
- Add new products with images
- Update existing products
- Delete products

### Shopping Cart
- Add products to cart
- Adjust product quantities
- Remove products from cart
- Cart persists across browser sessions via local storage
- Checkout process with stock quantity updates

### User Interface
- Responsive design using Bootstrap
- Toggle between light and dark themes
- Interactive navigation menu

## Future Enhancements
- User authentication and authorization
- Order history
- Payment gateway integration
- Product reviews and ratings
- Admin dashboard for analytics

