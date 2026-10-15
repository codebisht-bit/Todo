# Todo Application | Spring Boot

A simple and user-friendly Todo Management Application built using **Java, Spring Boot, Thymeleaf, Bootstrap, and PostgreSQL**. This project helps users manage their daily tasks through a web-based interface.

## 🚀 Features

- **Create Tasks** — Add new tasks to your todo list.
- **View Tasks** — Display tasks in a clean and organized interface.
- **Update Task Status** — Mark tasks as completed or pending.
- **Delete Tasks** — Remove tasks when they are no longer needed.
- **Database Integration** — Store task data using PostgreSQL.
- **Server-Side Rendering** — Render dynamic web pages using Thymeleaf.
- **Responsive UI** — Use Bootstrap for a clean, responsive interface.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Java | Backend programming |
| Spring Boot | Application framework |
| Spring Data JPA | Database operations |
| Hibernate | ORM and entity management |
| PostgreSQL | Relational database |
| Thymeleaf | Server-side HTML rendering |
| Bootstrap | Frontend styling |
| Maven | Build and dependency management |
| Git & GitHub | Version control |

## 📁 Project Structure

```text
todo/
├── src/
│   └── main/
│       ├── java/
│       │   └── com/app/todo/
│       │       ├── models/
│       │       ├── repository/
│       │       ├── service/
│       │       ├── controller/
│       │       └── TodoApplication.java
│       └── resources/
│           ├── templates/
│           ├── static/
│           └── application.properties
├── .gitignore
├── mvnw
├── mvnw.cmd
├── pom.xml
└── README.md
```

*Note: The structure above represents the intended organization; actual folders may differ slightly.*

## ⚙️ Prerequisites

Before running the project, make sure you have:

- Java JDK installed (matching the version configured in `pom.xml`).
- PostgreSQL installed and running.
- Git installed.
- An IDE such as Visual Studio Code or IntelliJ IDEA.

## 💻 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/codebisht-bit/Todo.git
cd Todo
```

### 2. Create the PostgreSQL database

Create a database named `todo-app` in PostgreSQL.

```sql
CREATE DATABASE "todo-app";
```

### 3. Configure database credentials

Configure your database connection using environment variables:

```properties
spring.application.name=todo
spring.datasource.url=${DB_URL}
spring.datasource.username=${DB_USERNAME}
spring.datasource.password=${DB_PASSWORD}
spring.jpa.hibernate.ddl-auto=update
spring.jpa.database-platform=org.hibernate.dialect.PostgreSQLDialect
```

Set `DB_URL`, `DB_USERNAME`, and `DB_PASSWORD` to match your local PostgreSQL configuration. Never commit real database passwords or other secrets to GitHub.

### 4. Run the application

On Windows, use the Maven wrapper:

```powershell
$env:DB_URL="jdbc:postgresql://localhost:5432/todo-app"
$env:DB_USERNAME="postgres"
$env:DB_PASSWORD="YOUR_LOCAL_PASSWORD"

.\mvnw.cmd spring-boot:run
```

Alternatively, import the project into your IDE and run `TodoApplication.java`.

### 5. Open the application

Once the application starts successfully, open:

http://localhost:8080

## 🗄️ Database

The application uses PostgreSQL to persist task information. Spring Data JPA and Hibernate handle database interactions and entity mapping.

## 🔮 Future Improvements

- User registration and authentication.
- Task due dates and priorities.
- Search, filtering, and sorting.
- Task categories and pagination.
- Automated tests and improved validation.

## 👨‍💻 Author

**Deepak Bisht**

GitHub: [@codebisht-bit](https://github.com/codebisht-bit)

## 📄 License

This project is available for learning and educational purposes. Add a formal open-source license if you want others to reuse or distribute it under specified terms.
