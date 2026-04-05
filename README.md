# Login-Reg - Spring MVC Login and Registration

A Java web application demonstrating user login, registration, form validation, and file upload functionality using Spring MVC with Hibernate-backed authentication against a MySQL database.

## Tech Stack

- **Java 8**
- **Spring Framework 4.0** (Core, Web MVC, ORM, JMS)
- **Hibernate 4.2** (ORM with MySQL dialect)
- **Hibernate Validator 4.0** (bean validation)
- **MySQL** (persistent user store)
- **JSP** (view layer)
- **Commons FileUpload** (multipart file uploads)
- **Maven** (build tool, WAR packaging)

## Project Structure

```
Login/src/main/
 ├── java/net/roseindia/
 │    ├── controllers/   # Spring MVC controllers
 │    │    ├── LoginController.java
 │    │    ├── RegistrationController.java
 │    │    ├── RegistrationValidation.java
 │    │    ├── UploadFileController.java
 │    │    ├── HelloWorldController.java
 │    │    ├── SimpleFormController.java
 │    │    └── ValidationController.java
 │    ├── dao/            # Data access layer (Hibernate)
 │    ├── form/           # Form-backing beans (LoginForm, Registration, etc.)
 │    ├── model/          # JPA entity (Users)
 │    └── service/        # Service layer (LoginService)
 ├── resources/
 │    └── applicationContext.xml   # Hibernate & DataSource config
 └── webapp/
      ├── index.jsp
      └── WEB-INF/
           ├── views/     # JSP pages (login, registration, upload, validation)
           ├── dispatcher-servlet.xml
           ├── messages.properties
           └── web.xml
```

### Features

- User login with database authentication via Hibernate
- User registration with server-side validation
- File upload with size validation
- Form validation examples (bean validation and custom validators)
- Hello world and simple form controller demos

## Build & Deploy

```bash
cd Login
mvn clean package
```

Deploy the generated `target/springmvclogin.war` to a servlet container such as Apache Tomcat 7+.

## Configuration

Database settings are in `src/main/resources/applicationContext.xml`. By default it connects to `jdbc:mysql://localhost:3306/springlogin` with username `root` and password `root`. Create the database and `users` table before deploying.
