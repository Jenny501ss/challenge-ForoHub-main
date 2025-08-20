# Foro Hub - Challenge Alura Latam & Oracle Next Education

Este proyecto es el resultado del **Challenge: Foro Hub** del programa **Oracle Next Education (ONE) + Alura Latam**, en el módulo de **Spring Framework**.  
El objetivo es construir una **API REST** para gestionar un foro de discusión, implementando autenticación, autorización, validaciones y operaciones CRUD.

---

## 🚀 Tecnologías utilizadas

- **Java 17**  
- **Spring Boot 3**  
- **Spring Data JPA**  
- **Spring Security**  
- **JWT (JSON Web Tokens)**  
- **Hibernate**  
- **MySQL**  
- **Maven**  
- **Flyway** (migraciones de base de datos)  
- **Swagger** (documentación de la API)  

---

## 📌 Funcionalidades principales

- **Autenticación y autorización** de usuarios mediante **JWT**.  
- **Gestión de tópicos del foro** (CRUD completo):  
  - Crear un nuevo tópico.  
  - Listar tópicos con paginación.  
  - Consultar detalles de un tópico específico.  
  - Actualizar información de un tópico.  
  - Eliminar un tópico (lógico/físico según implementación).  
- **Validaciones** de datos y reglas de negocio.  
- **Documentación automática** de la API con **Swagger UI**.  

---

## 📂 Estructura del proyecto

```
src
 └── main
     ├── java
     │   └── com.foro.hub
     │       ├── controller   # Controladores REST
     │       ├── domain       # Entidades y modelos
     │       ├── dto          # Data Transfer Objects
     │       ├── repository   # Interfaces de acceso a datos
     │       ├── security     # Configuración y filtros de seguridad
     │       └── service      # Lógica de negocio
     └── resources
         ├── application.properties  # Configuración
         └── db/migration            # Scripts de Flyway
```

---

## ⚙️ Configuración

### 1️⃣ Requisitos previos
- Tener instalado:
  - [Java 17+](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html)  
  - [Maven](https://maven.apache.org/)  
  - [MySQL](https://dev.mysql.com/downloads/)  

### 2️⃣ Clonar el repositorio
```bash
git clone https://github.com/Jenny501ss/challenge-ForoHub-main.git
cd challenge-ForoHub-main
```

### 3️⃣ Configurar la base de datos
En el archivo `application.properties` agrega tus credenciales de MySQL:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/forohub
spring.datasource.username=tu_usuario
spring.datasource.password=tu_contraseña
spring.jpa.hibernate.ddl-auto=validate
spring.jpa.show-sql=true

# JWT
api.security.secret=mi_clave_secreta
```

### 4️⃣ Ejecutar el proyecto
```bash
mvn spring-boot:run
```

La aplicación estará disponible en:  
👉 `http://localhost:8080`

---

## 🔑 Endpoints principales

### Autenticación
- `POST /login` → Genera token JWT

### Tópicos
- `POST /topicos` → Crear un nuevo tópico  
- `GET /topicos` → Listar todos los tópicos (con paginación)  
- `GET /topicos/{id}` → Obtener detalles de un tópico  
- `PUT /topicos/{id}` → Actualizar un tópico  
- `DELETE /topicos/{id}` → Eliminar un tópico  

---

## 📖 Documentación con Swagger

Una vez levantada la app, accede a la documentación en:  
👉 `http://localhost:8080/swagger-ui/index.html`

---

## 👩‍💻 Autor

**Jenny Joseline Mamani Choque**  
📧 [yenny501ss@gmail.com](mailto:yenny501ss@gmail.com)  
💼 [LinkedIn](https://www.linkedin.com/in/jenny-joseline-mamani-choque-07963593)

---

✨ Este proyecto forma parte del programa **Oracle Next Education (ONE) + Alura Latam**.  


