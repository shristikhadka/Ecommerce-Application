SpringEcom
A robust e-commerce backend application built with Spring Boot.

Features
Complete product management with CRUD operations
Image upload and retrieval for products
Flexible search functionality across multiple fields (name, description, brand, category)
RESTful API endpoints with proper HTTP status code handling
PostgreSQL integration for data persistence

Technology Stack
Java 21
Spring Boot 3.4.3
Spring Data JPA
PostgreSQL
Maven

API Endpoints
MethodURLDescriptionGET/api/productsGet all productsGET/api/product/{id}Get product by IDGET/api/product/{id}/imageGet product image by product IDPOST/api/productAdd a new productPUT/api/product/{id}Update an existing productDELETE/api/product/{id}Delete a productGET/api/products/searchSearch products by keyword
Setup and Installation

Prerequisites
Java 21
PostgreSQL
Maven

Database Configuration
Update the application.properties file with your PostgreSQL database credentials:
propertiesspring.datasource.url=jdbc:postgresql://localhost:5432/your_database
spring.datasource.username=your_username
spring.datasource.password=your_password
Build and Run
bash# Clone the repository
git clone https://github.com/shristikhadka/Ecommerce-Application

# Navigate to project directory
cd SpringEcom

# Build the project
./mvnw clean install

# Run the application
./mvnw spring-boot:run
The application will start on http://localhost:8080
Project Structure
src/main/java/com/telusko/SpringEcom/
  ├── controller/        # REST controllers
  ├── model/             # Entity classes
  ├── repo/              # Repository interfaces
  ├── service/           # Business logic
  └── SpringEcomApplication.java  # Main application class
Contributing
Contributions are welcome! Please feel free to submit a Pull Request.
