# Polis Hospital Management System

## Project Overview

The **Polis Hospital Management System** is a backend application designed to manage departments, patients, admissions, clinical records, and error management for a hospital. Built using **Java Spring Boot**, this system utilizes a **relational database** (MySQL/PostgreSQL) to store and manage data related to hospital operations.

The system supports various features such as:

- Managing departments.
- Managing patients, including their admission and discharge details.
- Maintaining clinical records for patients.
- Error management with clear exception handling.
- Unit testing for services and repositories.

---

## Key Features

- **Department Management**: Manage hospital departments, ensuring that they cannot be deleted if associated with patients.
- **Patient Management**: Handle patient admissions, discharges, and department changes. Each patient can only be assigned to one department.
- **Admission/Discharge Management**: Record reasons for discharge (e.g., recovery, transfer, death).
- **Clinical Records**: Free-text input for medical notes regarding patients.
- **Error Management**: Provides clear error messages and handles server-side exceptions.
- **Unit Testing**: Includes unit tests for services, repositories, and controllers using **JUnit**.

---

## Technologies Used

- **Backend Framework**: Spring Boot (Java)
- **Database**: MySQL or PostgreSQL
- **Testing**: JUnit
- **Build Tool**: Maven or Gradle
- **Version Control**: Git, GitHub

---

## Installation Guide

Follow the steps below to set up the Hospital Management System on your local machine:

### 1. **Clone the Repository**

````bash
git clone https://github.com/ergishasani/polis-hospital-management.git
cd polis-hospital-management


### 2. **Setup Database**

- Set up a **MySQL** or **PostgreSQL** database for the project.
- Update the `application.properties` file in `src/main/resources` to match your database configuration.

Example (MySQL):

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/hospital_db
spring.datasource.username=root
spring.datasource.password=password
spring.jpa.hibernate.ddl-auto=update
spring.jpa.database-platform=org.hibernate.dialect.MySQL5InnoDBDialect
````

### 3. **Build the Project**

If you're using **Maven**:

```bash
mvn clean install
```

Or **Gradle**:

```bash
gradle build
```

### 4. **Run the Application**

Start the Spring Boot application:

```bash
mvn spring-boot:run
```

Or if you're using Gradle:

```bash
gradle bootRun
```

The application should now be running on `http://localhost:8080`.

---

## API Documentation

This project exposes RESTful APIs to interact with the system. Below is a brief overview of the key endpoints:

### 1. Department API

- **GET** `/departments`: Get all departments.
- **POST** `/departments`: Create a new department.
- **GET** `/departments/{id}`: Get department details by ID.
- **DELETE** `/departments/{id}`: Delete a department.

### 2. Patient API

- **GET** `/patients`: Get all patients.
- **POST** `/patients`: Add a new patient.
- **GET** `/patients/{id}`: Get patient details by ID.
- **DELETE** `/patients/{id}`: Delete a patient.

### 3. Admission API

- **GET** `/admissions`: Get all admissions.
- **POST** `/admissions`: Add a new admission.
- **GET** `/admissions/{id}`: Get admission details by ID.

### 4. Clinical Record API

- **GET** `/clinical-records`: Get all clinical records.
- **POST** `/clinical-records`: Add a new clinical record.

---

## Testing

Unit tests are written for the core services and repositories. To run the tests:

### 1. **Using Maven**:

```bash
mvn test
```

### 2. **Using Gradle**:

```bash
gradle test
```

---

## Contributing

We welcome contributions to improve the project! Please follow these steps if you'd like to contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit them (`git commit -am 'Add new feature'`).
4. Push your branch to your forked repository (`git push origin feature-branch`).
5. Open a pull request with a detailed explanation of the changes.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Contact

For any inquiries or issues, please contact:

- **Email**:
- **GitHub**: [Ergis Hasani](https://github.com/ergishasani/polis-hospital-management)
- **GitHub**: [Hysnie Likaj](https://github.com/nia-likaj/polis-hospital-management)

---

---

Just copy everything above and paste it into your `README.md` file. Make sure to replace `your-username` with your actual GitHub username and update any specific details for your project!
