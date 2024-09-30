# E-Commerce Web Application

This project is a backend implementation of an e-commerce web application built using the Java Spring Boot framework. The application allows users to retrieve product information from a database and enables sellers to update product details.

## Features

- Retrieve a list of products available in the database.
- Sellers can update the details of a specific product.
- Backend services that handle CRUD operations for product management.

## Technologies Used

- **Java Spring Boot**: Framework for building the backend REST API.
- **PostgreSQL**: Database system used to store product details.
- **Hibernate**: Object-Relational Mapping (ORM) framework to map Java objects to database tables.
- **Apache Tomcat**: Server for hosting and running the application.
- **Lombok**: Used to reduce boilerplate code.
- **Maven**: Dependency management tool for managing external libraries.

## Project Structure

```
├── SpringEcom               # Main project directory
│   ├── controller            # Contains the controllers for handling HTTP requests
│   │   └── ProductController.java  # Handles product-related requests
│   ├── model                 # Contains the data model classes
│   │   └── Product.java       # Product entity class
│   ├── repo                  # Repository layer for database interactions
│   │   └── ProductRepo.java   # Repository interface for product data
│   ├── service               # Contains the service layer business logic
│   │   └── ProductService.java # Service class for product operations
│   └── SpringEcomApplication.java # Main entry point of the application
├── README.md                 # Project documentation
```

## Setup Instructions

### Prerequisites

- Java 11 or higher
- PostgreSQL (with a running instance)
- Maven 3.6.x or higher
- Apache Tomcat (optional, if not using embedded server)

### Database Setup

1. Install PostgreSQL and create a new database for the project.
   
2. Update the `application.properties` file to configure the database connection.

   ```properties
   spring.datasource.url=jdbc:postgresql://localhost:5432/<your-database-name>
   spring.datasource.username=<your-username>
   spring.datasource.password=<your-password>
   spring.jpa.hibernate.ddl-auto=update
   ```

### Build and Run

1. Clone the repository to your local machine:
   
   ```bash
   git clone <repository-url>
   cd E-commerce-web-Application-main
   ```

2. Build the project using Maven:

   ```bash
   mvn clean install
   ```

3. Run the Spring Boot application:

   ```bash
   mvn spring-boot:run
   ```

   The application should now be running at `http://localhost:8080`.

### API Endpoints

The application exposes the following REST API endpoints:

- **GET /products**: Retrieve a list of products.
- **GET /products/{id}**: Retrieve product details by product ID.
- **POST /products**: Add a new product (Seller only).
- **PUT /products/{id}**: Update an existing product (Seller only).
- **DELETE /products/{id}**: Delete a product by ID (Seller only).

### Lombok Configuration

This project uses Lombok annotations to reduce boilerplate code. Make sure to install Lombok in your IDE:

- For **Eclipse**, install the Lombok plugin from the Eclipse Marketplace.
- For **IntelliJ IDEA**, enable annotation processing under `Preferences > Build, Execution, Deployment > Compiler > Annotation Processors`.

### Running Tests

To run the unit tests, use the following command:

```bash
mvn test
```

## Contributing

Feel free to contribute to this project by submitting issues or pull requests.

## License

This project is licensed under the MIT License.


License
This project is licensed under the MIT License. See the LICENSE file for details.

Contact
If you have any questions or would like to reach out, feel free to email me at bheemhepte@gmail.com or connect with me on LinkedIn.

