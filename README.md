# ShopEase - E-commerce Store

Team: Abbaz Meirzhan, Temirbek Akzhol

Figma design: https://www.figma.com/design/8ITURNS5deKCwaJaK9JX6N/Untitled?node-id=0-1&t=n0SROHlZR4bniJ7C-1

GitHub repository: https://github.com/KayenFenix/ShopEase

Project description

ShopEase is a full-stack online store built with Java Spring Boot that lets customers browse a product catalog, search and filter items, add products to a shopping cart, and place orders through a simple checkout process. Registered customers can manage their profile, track order history, and follow the status of each order. Administrators get a dedicated panel for managing products, categories, stock levels, and incoming orders.

The application follows a layered Spring architecture (Controller, Service, Repository, Database) and stores all data in a PostgreSQL database through Spring Data JPA. Authentication and role-based authorization are handled by Spring Security, so customers and administrators see only the functions that belong to their role. The user interface is rendered with Thymeleaf and styled with HTML, CSS, and JavaScript, following a clickable Figma prototype designed before development.

The project demonstrates the main skills of the course: designing entities and relations, implementing business logic in the service layer, validating user input, securing pages by role, and testing the application with JUnit and Postman.

Target users

- Customers who want to buy products online quickly and track their orders.
- Administrators and store managers who maintain products, prices, stock, and process orders.
- Small businesses that need a simple store of their own.

Functional requirements

1. Registration and login with hashed passwords (BCrypt).
2. Role-based access: CUSTOMER and ADMIN.
3. Product catalog with images, price, description, category filter, search, and pagination.
4. Product details page with stock availability and an Add to cart button.
5. Shopping cart: add, remove, change quantity, see the total price.
6. Checkout and orders: delivery details, order placement, automatic stock reduction.
7. Order history and statuses: NEW, PAID, SHIPPED, DELIVERED, CANCELLED.
8. Admin product management: create, edit, delete products and categories, update stock and prices.
9. Admin order management: view all orders and change their status.
10. Input validation and error handling with clear messages.

Technology stack

- Programming language: Java 17
- Backend framework: Spring Boot
- Web layer: Spring MVC / Spring Web
- Frontend: Thymeleaf, HTML, CSS, JavaScript
- Database: PostgreSQL
- Persistence: Spring Data JPA / Hibernate
- Build tool: Maven
- Version control: Git / GitHub
- Testing: JUnit, Postman
- Design: Figma

Spring Boot dependencies

- Spring Web
- Spring Data JPA
- Thymeleaf
- PostgreSQL Driver
- Lombok
- Spring Validation
- Spring Security
- Spring Boot Starter Test

Architecture

Frontend -> Controller -> Service -> Repository -> Database (PostgreSQL)

- Frontend: Thymeleaf pages, CSS, JavaScript. Displays pages and sends user actions to the server.
- Controller: processes HTTP requests and returns views or responses.
- Service: implements business logic (cart total, stock check, order creation, order status).
- Repository: handles database access through Spring Data JPA.
- Entity / Model: represents application data (User, Role, Category, Product, Cart, CartItem, Order, OrderItem).
- Database: stores all information in PostgreSQL tables with relations and constraints.

Figma screens

Home, Product Catalog, Product Details, Shopping Cart, Checkout, Order Confirmation, Login / Registration, My Orders, Admin Panel, Customer Support.

Team responsibilities

- Abbaz Meirzhan, Backend / Database Developer: database design, JPA entities, repositories, service layer, Spring Validation, JUnit tests, GitHub repository setup.
- Temirbek Akzhol, Frontend / UX/UI and Integration Developer: Figma design and prototype, Thymeleaf views, HTML/CSS/JavaScript, controllers, Spring Security configuration, Postman and integration testing.

Development roadmap

1. Project requirements and planning: both students.
2. UX/UI design: Temirbek Akzhol.
3. Spring Boot project setup: Abbaz Meirzhan.
4. Database and entity development: Abbaz Meirzhan.
5. Repository, Service, Controller implementation: Abbaz Meirzhan (Repository, Service), Temirbek Akzhol (Controller, Security).
6. Frontend development: Temirbek Akzhol.
7. Integration and testing: Abbaz Meirzhan (JUnit), Temirbek Akzhol (Postman, integration).
8. Final Exam presentation and demonstration: both students.
