# Bautista-post1-u7
Unidad 7: Patrones Arquitectónicos I Post-Contenido 1

## Descripción
Este proyecto implementa un sistema de gestión de tareas utilizando Spring Boot y arquitectura en capas. Permite crear, listar, actualizar y eliminar tareas mediante una API REST.

---

## Tecnologías utilizadas
- Java 17+
- Spring Boot
- Spring Web
- Spring Data JPA
- H2 Database
- Maven

---

## Arquitectura
El proyecto está organizado siguiendo una arquitectura en capas:

com.example.tareas/
- controller/ → Capa de presentación (API REST)
- service/ → Lógica de negocio
- repository/ → Acceso a datos
- domain/
  - model/ → Entidades
  - exceptions → Excepciones de negocio

---

## Endpoints disponibles

### Listar tareas
GET /api/tareas

### Buscar tarea por ID
GET /api/tareas/{id}

### Crear tarea
POST /api/tareas

Ejemplo JSON:
{
  "titulo": "Estudiar",
  "descripcion": "Spring Boot"
}

### Cambiar estado
PATCH /api/tareas/{id}/estado?estado=COMPLETADA

### Eliminar tarea
DELETE /api/tareas/{id}

---

## Validaciones
- El campo `titulo` es obligatorio

---

## Manejo de errores
- 404 Not Found → Tarea no encontrada
- 400 Bad Request → Error de validación

---

## Base de datos H2
- Consola: http://localhost:8080/h2-console
- JDBC URL: jdbc:h2:mem:testdb
- Usuario: sa
- Contraseña: (vacío)

---

## Ejecución del proyecto

  bash
mvn clean install
mvn spring-boot:run

## Pruebas con curl ##
<img width="1260" height="507" alt="image" src="https://github.com/user-attachments/assets/2d87358f-af0c-46b0-ae78-0ba2ab2d74cb" />

## Evidendicias ##
<img width="1302" height="835" alt="image" src="https://github.com/user-attachments/assets/d1f13c70-1807-49a5-b530-6cba30dd362d" />
<img width="416" height="772" alt="image" src="https://github.com/user-attachments/assets/644fc042-3c99-485c-9a1a-2909e734494c" />
