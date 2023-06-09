# Taxi Service

This is a simple application that implements a taxi service. With this project, you can create, remove, and update cars, drivers and manufacturers, as well as assign drivers to cars. To ensure the security and confidentiality of users, the project implements a user identification process and grants permission to access resources.

The application is developed based on a 3-tier architecture:
- Presentation layer
- Application layer
- Data access layer

# Features
- Login/Logout
- Create new Driver/Car/Manufacturer
- Display All Drivers/Cars/Manufacturers
- Delete Driver/Car/Manufacturer
- Add Driver to Car
- Get Current Cars For Driver

# Project Structure
- Controllers :
  - AddCarController            - POST /cars/add
  - AddDriverToCarController    - POST /cars/drivers/add 
  - DeleteCarController         - GET /cars/delete
  - GetAllCarsController        - GET /cars
  - AddDriverController         - POST /drivers/add
  - DeleteDriverController      - GET /drivers/delete
  - GetAllDriversController     - GET /drivers
  - GetMyCurrentCarsController  - GET /drivers/cars
  - AddManufacturerController   - POST /manufacturers/add
  - DeleteManufacturerController - GET /manufacturers/delete
  - GetAllManufacturersController - GET /manufacturers
  - IndexController               - GET /
  - LoginController              - POST /login
  - LogoutController             -GET /logout
- DAO : interfaces and their implementations are responsible for connection with the database and performing CRUD operations.
- Model :
  - Car model
  - Driver model
  - Manufacturer model
- Service : interfaces and their implementations are responsible for the business logic of the application.
- Util : ConnectionUtil is responsible for establishing a connection to the database.
- Web/filter : AuthenticationFilter is responsible for the authentication process.
- Resources : configuration files and database scripts
- Webapp/WEB-INF/views : configuration files for the web application, web resources such as CSS and JSP files

# Used Technologies
- Java  17.0.6
- Tomcat 9.0.50.
- JDBC 8.0
- Maven 3.8.7
- Maven Checkstyle Plugin 3.1.1
- MySQL 8.0.32
- Servlet 4.0.1
- JSTL 1.2

 # How to run
- Configure Apache Tomcat for your IDE
- Install MySQL and MySQL Workbench
- Clone this remote repository to your local repository
- Create a schema by using the script from resources/init_db.sql in MySQL Workbench
- In the taxi/util/ConnectionUtil change the URL, USERNAME and PASSWORD
- Deploy this project using Tomcat local server 