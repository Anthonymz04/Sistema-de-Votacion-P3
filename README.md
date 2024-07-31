Sistema-de-Votacion-P3
Descripción
El Sistema de Votación ApiRestFull es una aplicación desarrollada en Java utilizando Spring Boot. Proporciona una API RESTful para gestionar un sistema de votación que incluye la administración de candidatos, estudiantes, mesas electorales y votos. Como herramienta extra se encuentra Insomnia y ingreso mediante archivo Json.

Características
Gestión de candidatos.
Gestión de estudiantes.
Gestión de mesas electorales.
Registro y consulta de votos.
Requisitos
Java 11 o superior
Maven 3.6.0 o superior
MySQL 5.7 o superior
Instalación
Clonar el repositorio
bash
Copiar código
git clone https://github.com/tu-usuario/Sistema-de-Votacion-P3.git
cd Sistema-de-Votacion-P3
Configurar la base de datos
Crea una base de datos en MySQL:

sql
Copiar código
CREATE DATABASE sistema_votacion;
Configura las credenciales de la base de datos en el archivo application.properties ubicado en src/main/resources:

properties
Copiar código
spring.datasource.url=jdbc:mysql://localhost:3306/sistema_votacion
spring.datasource.username=tu_usuario
spring.datasource.password=tu_contraseña
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL5Dialect
Construir y ejecutar la aplicación
bash
Copiar código
mvn clean install
mvn spring-boot:run
La aplicación estará disponible en http://localhost:8080.

Endpoints
Candidatos
GET /api/v1/candidatos - Obtener todos los candidatos.
POST /api/v1/candidatos - Crear un nuevo candidato.

Estudiantes
GET /api/v1/estudiantes - Obtener todos los estudiantes.
POST /api/v1/estudiantes - Crear un nuevo estudiante.

Mesas Electorales
GET /api/v1/mesas - Obtener todas las mesas electorales.
POST /api/v1/mesas - Crear una nueva mesa electoral.

Votos
GET /api/v1/votos - Obtener todos los votos.
POST /api/v1/votos - Registrar un nuevo voto.
