# Hibernate Library

This repository contains a project utilizing Hibernate for Object-Relational Mapping (ORM) in a Java application. The project is built using Java EE7, JDK 8, GlassFish 5, and integrates Hibernate for efficient database management.

## Features

- ORM with Hibernate
- Database management and configuration using `hibernate.cfg.xml`
- Integration with Java EE7 and GlassFish 5

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Java Development Kit (JDK) 8
- GlassFish Server 5
- Apache Maven (optional for dependency management)
- An IDE like IntelliJ IDEA, Eclipse, or NetBeans
- A database (e.g., MySQL, PostgreSQL)

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/DisuraAberathna/Hibernate-Libraries.git
   ```

2. **Navigate to the project directory:**

   ```bash
   cd Hibernate-Library
   ```

3. **Configure Hibernate:**

   Update the `hibernate.cfg.xml` file located in the `src/main/resources` directory with your database credentials and settings.

4. **Deploy the application:**

   Deploy the project on GlassFish 5 by either using your IDE or manually through the GlassFish admin console.

5. **Run the application:**

   Access the application through your browser at `http://localhost:8080/your-app-context`.

## Configuration

### Hibernate Configuration (`hibernate.cfg.xml`)

Ensure you have the correct database settings:

```xml
<hibernate-configuration>
    <session-factory>
        <!-- Database connection settings -->
        <property name="hibernate.connection.driver_class">com.mysql.cj.jdbc.Driver</property>
        <property name="hibernate.connection.url">jdbc:mysql://localhost:3306/your_database</property>
        <property name="hibernate.connection.username">your_username</property>
        <property name="hibernate.connection.password">your_password</property>

        <!-- JDBC connection pool settings -->
        <property name="hibernate.c3p0.min_size">5</property>
        <property name="hibernate.c3p0.max_size">20</property>
        <property name="hibernate.c3p0.timeout">300</property>
        <property name="hibernate.c3p0.max_statements">50</property>
        <property name="hibernate.c3p0.idle_test_period">3000</property>

        <!-- SQL dialect -->
        <property name="hibernate.dialect">org.hibernate.dialect.MySQLDialect</property>

        <!-- Echo all executed SQL to stdout -->
        <property name="hibernate.show_sql">true</property>

        <!-- Drop and re-create the database schema on startup -->
        <property name="hibernate.hbm2ddl.auto">update</property>
    </session-factory>
</hibernate-configuration>
```

## Usage

After deploying, navigate to the application's base URL to start using the Hibernate Library. You can manage database interactions and perform various operations as per the application's design.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
