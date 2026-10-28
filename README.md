# Product Catalog REST API

A professional RESTful backend built with Java and Spring Boot for managing a product catalog. The project demonstrates CRUD operations, request/response models, and persistence with an in-memory H2 database.

## 📦 Features

- Create new products
- Retrieve a single product or list all products
- Update existing products
- Delete products
- H2 in-memory database for easy testing
- Example requests included (curl)

## 🛠 Technologies

- Java 17+
- Spring Boot
- Maven
- H2 Database
- Spring Web

## 📁 Project Structure

```text
src/
└── main/
    └── java/com/springstarter/first_rest_api/
        ├── FirstRestApiApplication.java
        └── product/
            ├── api/
            │   ├── ProductController.java
            │   ├── request/
            │   │   ├── ProductRequest.java
            │   │   └── UpdateProductRequest.java
            │   └── response/
            │       └── ProductResponse.java
            ├── domain/
            │   └── Product.java
            └── repository/
                └── ProductRespository.java
```

## 🚀 Quick Start

### Prerequisites

- Java 17 or newer
- Maven (or use the included Maven wrapper)

### Run locally

Clone the repository and run:

```bash
git clone https://github.com/hereAlisher/secondtask.git
cd secondtask
./mvnw spring-boot:run
```

The application starts on http://localhost:8080 by default.

## 🔗 API Endpoints

| Method | Endpoint           | Description             |
|--------|--------------------|-------------------------|
| GET    | /products          | Get all products        |
| GET    | /products/{id}     | Get product by ID       |
| POST   | /products          | Create a new product    |
| PUT    | /products/{id}     | Update existing product |
| DELETE | /products/{id}     | Delete a product        |

### Example curl requests

- Create
```bash
curl -X POST http://localhost:8080/products \
  -H "Content-Type: application/json" \
  -d '{"name":"Example Product","price":19.99,"description":"A sample product."}'
```

- Get all
```bash
curl http://localhost:8080/products
```

- Get by ID
```bash
curl http://localhost:8080/products/1
```

- Update
```bash
curl -X PUT http://localhost:8080/products/1 \
  -H "Content-Type: application/json" \
  -d '{"name":"Updated Name","price":29.99,"description":"Updated description."}'
```

- Delete
```bash
curl -X DELETE http://localhost:8080/products/1
```

## 🗃 H2 Database Console

The app uses an H2 in-memory database. Access the console at:

http://localhost:8080/h2-console

- JDBC URL: `jdbc:h2:mem:testdb`
- Username: `sa`
- Password: (leave blank)

## 🧪 Testing

Use Postman, curl, or any HTTP client to test endpoints. Because the database is in-memory, data will be reset when the application restarts.

## 📸 Screenshots

Here are the screenshots:
<img width="1908" height="1068" alt="database" src="https://github.com/user-attachments/assets/313083b7-46b7-4c86-b20f-7c462102e3fa" />
<img width="1919" height="850" alt="delete" src="https://github.com/user-attachments/assets/d0d3d936-cb91-411a-8e64-db12f28c4a7d" />
<img width="1886" height="1069" alt="get" src="https://github.com/user-attachments/assets/fa9067d7-4813-4c9d-ae3a-a725c83c9aeb" />
<img width="1894" height="1062" alt="get-all" src="https://github.com/user-attachments/assets/b65391a3-cdb3-42dd-a1eb-bc5a88ecbe0d" />
<img width="1883" height="1055" alt="post" src="https://github.com/user-attachments/assets/d352b416-672a-4a9c-af07-f62506105f63" />
<img width="1887" height="1063" alt="put" src="https://github.com/user-attachments/assets/41bf3f3e-5108-4496-882a-bfd594007b80" />

## Contributing

Contributions are welcome. If you plan to add functionality or fix bugs:

1. Fork the repository
2. Create a feature branch: `git checkout -b feat/your-feature`
3. Commit your changes and push
4. Open a pull request describing your changes