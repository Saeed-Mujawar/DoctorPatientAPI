<h1 align = "center"> Doctor Patient Api </h1>

* This is a backend application for a Doctor-Patient management system. It provides APIs to add doctors, add patients with their symptoms, and suggest doctors based on patient's symptoms and location.

## Technologies Used
* Java
* Spring Boot

* MySQL




## Database Configuration
* To connect to a MySQL database, update the application.properties file with the appropriate database URL, username, and password. The following properties need to be updated:
```
spring.datasource.driverClassName=com.mysql.cj.jdbc.Driver
spring.datasource.url=jdbc:mysql://localhost:3306/doctorpatientdb
spring.datasource.username=<your_database_username>
spring.datasource.password=<your_database_password>
spring.jpa.show-sql = true
spring.jpa.hibernate.ddl-auto = update

spring.jpa.properties.hibernate.show_sql=true
spring.jpa.properties.hibernate.use_sql_comments=true
spring.jpa.properties.hibernate.format_sql=true

```

>## Data flow
In this project, we have four layers-
* **Controller** - The controller layer handles the HTTP requests, translates the JSON parameter to object, and  the request and transfer it to the business (service) layer. In short, it consists of views i.e., frontend part.
* **Service** -The business layer handles all the business logic. It consists of service classes and uses services provided by data access layers.
* **Repository** - This layer mainatains the CRUD operations are performed
* **Model** - This layer consists basically the class level things- the various classes required for the project and these classes consists the attributes to be stored.

>## API Endpoints

### Adding a Doctor
* Endpoint: POST /api/doctors
* Request Body: JSON representing the doctor details
* Example:

```
{
  "id": 1,
  "name": "Saeed",
  "city": "NOIDA",
  "email": "saeed@example.com",
  "phoneNumber": "8989898989",
  "speciality": "ORTHOPEDIC"
}

```

### Adding a Patient
* Endpoint: POST /api/patients
* Request Body: JSON representing the patient details
* Example:
```
{
  "id": 1,
  "name": "Jane Smith",
  "city": "NOIDA",
  "email": "janesmith@example.com",
  "phoneNumber": "9999999999",
  "symptom": "BACK_PAIN"
}

```

## Project Summary
The Doctor-Patient Management System is a backend application designed to facilitate the management of doctors and patients in a healthcare setting.
The system provides various APIs to add doctors, 
add patients with their symptoms, and suggest doctors based on patient symptoms and location.
