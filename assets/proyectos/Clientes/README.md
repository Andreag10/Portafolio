Proyecto de Gestión de Usuarios

Este proyecto es una aplicación web completa desarrollada con Angular para el frontend y Spring Boot para el backend. Permite realizar operaciones CRUD (Crear, Leer, Actualizar y Eliminar) sobre una lista de usuarios almacenados en una base de datos PostgreSQL.

Tecnologías Utilizadas

Frontend:

Angular (Framework para el desarrollo web)

TypeScript (Lenguaje de programación)

HTML y CSS (Diseño y estructura)

Angular Material (opcional para mejorar estilos)

HTTPClient (para la comunicación con el backend)

Backend:

Spring Boot (Framework para la creación de la API)

Java (Lenguaje de programación)

Spring Data JPA (Manejo de base de datos)

PostgreSQL (Base de datos)

Maven (Gestor de dependencias)

Instalación y Configuración Paso a Paso

Requisitos previos

Asegúrate de tener instalado en tu sistema:

Node.js y Angular CLI

Java JDK 17 o superior

Maven

PostgreSQL

Paso 1: Configurar la base de datos PostgreSQL

Abre PostgreSQL y crea una base de datos llamada usuarios_db.

Configura las credenciales en el archivo application.properties del backend:

spring.datasource.url=jdbc:postgresql://localhost:5432/usuarios_db
spring.datasource.username=tu_usuario
spring.datasource.password=tu_contraseña

Paso 2: Configurar y ejecutar el backend (Spring Boot)

Clona el repositorio y accede al directorio del backend:

git clone <URL_DEL_REPOSITORIO>
cd backend

Compila y ejecuta el backend con Maven:

mvn spring-boot:run

El backend estará disponible en http://localhost:8080/api/usuarios.

Paso 3: Configurar y ejecutar el frontend (Angular)

Clona el repositorio y accede al directorio del frontend:

git clone <URL_DEL_REPOSITORIO>
cd frontend

Instala las dependencias necesarias:

npm install

Inicia el servidor de desarrollo de Angular:

ng serve

Abre http://localhost:4200/ en tu navegador para ver la aplicación en funcionamiento.

Endpoints del Backend

Método

Endpoint

Descripción

GET

/api/usuarios

Obtener todos los usuarios

GET

/api/usuarios/{id}

Obtener un usuario por ID

POST

/api/usuarios

Crear un nuevo usuario

PUT

/api/usuarios/{id}

Actualizar un usuario

DELETE

/api/usuarios/{id}

Eliminar un usuario

Funcionalidades del Proyecto

Lista de Usuarios: Visualiza la lista de usuarios registrados.

Agregar Usuario: Permite agregar un nuevo usuario con nombre y correo.

Editar Usuario: Modifica la información de un usuario existente.

Eliminar Usuario: Borra un usuario de la base de datos.

Interfaz Amigable: Diseño sencillo y funcional para facilitar la gestión de usuarios.

Estructura del Proyecto

Backend:

backend/
├── src/main/java/com/adso/Cliente/
│   ├── Usuario.java
│   ├── UsuarioController.java
│   ├── UsuarioServicio.java
│   ├── UsuarioRepository.java
└── ...

Frontend:

frontend/
├── src/app/
│   ├── components/
│   │   ├── usuario-form/
│   │   ├── usuarios-lista/
│   ├── services/
│   │   ├── usuario.service.ts
│   ├── models/
│   │   ├── usuario.model.ts
└── ...

Uso de la Aplicación

Abre http://localhost:4200/ en tu navegador.

Visualiza la lista de usuarios registrados.

Usa el formulario para agregar, editar o eliminar usuarios.

Contribuciones

Si deseas contribuir, por favor sigue estos pasos:

Haz un fork del repositorio.

Crea una nueva rama (git checkout -b feature-nueva).

Realiza tus cambios y súbelos (git commit -m "Añadir nueva funcionalidad").

Sube los cambios a tu repositorio (git push origin feature-nueva).

Crea un Pull Request.