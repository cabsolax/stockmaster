# 📦 StockMaster

Sistema de **gestión de inventarios y ventas** desarrollado con **Spring Boot**, siguiendo principios de **arquitectura MVC**, persistencia con **Spring Data JPA / Hibernate**, servicios **REST**, validaciones, seguridad con **Spring Security + JWT**, y documentación de API con **Swagger (OpenAPI)**.

---

## 🎯 Objetivo del proyecto
Diseñar e implementar una aplicación web empresarial que permita administrar:
- Catálogo de productos y categorías
- Control de inventarios en almacenes
- Movimientos de stock
- Registro de clientes, pedidos y pagos
- Gestión de compras a proveedores
- Reportes básicos de operaciones
- Seguridad y control de acceso por roles

---

## 🛠️ Tecnologías utilizadas
- **Java 17**
- **Spring Boot 3.5.5**
- **Spring Data JPA + Hibernate**
- **Spring Security + JWT**
- **Spring Validation (javax.validation)**
- **Swagger / OpenAPI (springdoc)**
- **MySQL / PostgreSQL**
- **Maven**
- **Git & GitHub**

---


## 📂 Estructura del repositorio
stockmaster/
├─ backend/ # Código fuente de la aplicación Spring Boot
│ ├─ src/main/java/com/acme/stockmaster/
│ │ ├─ config/ # Seguridad, JWT, Swagger config
│ │ ├─ controller/ # Controladores REST
│ │ ├─ dto/ # Objetos de transferencia
│ │ ├─ entity/ # Entidades JPA
│ │ ├─ exception/ # Manejo de errores
│ │ ├─ repository/ # Repositorios JPA
│ │ └─ service/ # Servicios de negocio
│ └─ src/main/resources/ # application.yml, data.sql, schema.sql
│
├─ docs/
│ ├─ fase1/
│ │ ├─ analisis-diseno.md # Documento formal Fase 1
│ │ ├─ diagramas/ # UML, ERD
│ │ └─ mockups/ # Interfaces simuladas
│ └─ fase2/ # Documentación de implementación
│
├─ pom.xml
└─ README.md



yaml
Copiar código

---

## 🚀 Ejecución local
### Requisitos previos
- JDK 17+
- Maven 3.9+
- MySQL o PostgreSQL corriendo localmente

### Configuración base de datos
En src/main/resources/application.yml`:
yaml
spring:
  datasource:
    url: jdbc:postgresql://localhost:5432/stockmaster
    username: postgres
    password: postgres
  jpa:
    hibernate:
      ddl-auto: update
    show-sql: true
    properties:
      hibernate.format_sql: true
Ejecutar aplicación
bash
Copiar código
./mvnw spring-boot:run
📖 Documentación de API
Una vez en ejecución, acceder a:

Swagger UI:
👉 http://localhost:8080/swagger-ui/index.html

OpenAPI JSON:
👉 http://localhost:8080/v3/api-docs

👥 Roles y seguridad
ADMIN: acceso total

VENTAS: pedidos, pagos y clientes

ALMACEN: inventario, movimientos y compras

📅 Cronograma
Fase 1 (5 de septiembre): Análisis, diseño, diagramas, mockups, planificación.

Fase 2 (31 de octubre): Implementación funcional, pruebas, defensa del proyecto.

👨‍💻 Autores
Proyecto realizado por:

Carlos Alexander Caballeros Cruz (@cabsolax)
