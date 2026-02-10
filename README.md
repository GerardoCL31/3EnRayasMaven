# 🎮 Actividad 1 – Despliegue de aplicación Spring Boot con Docker y Render

## 📌 Descripción del proyecto

Este proyecto consiste en el desarrollo y despliegue de una **aplicación web con Spring Boot** basada en el juego clásico **3 en raya (Tic-Tac-Toe)** para **dos jugadores**.

El objetivo principal de la actividad es practicar un **flujo completo de despliegue**, incluyendo la creación de la aplicación, su contenerización con Docker, la publicación de la imagen en Docker Hub y el despliegue en Render con un dominio personalizado.

---

## 🎯 Funcionalidades de la aplicación

- Juego de 3 en raya para dos jugadores (X y O)
- Interfaz web moderna, centrada y responsiva
- Control de turnos
- Detección automática de ganador y empates
- Contador de partidas
- Botón para reiniciar el juego

La lógica del juego se ejecuta en **JavaScript** en el navegador, mientras que **Spring Boot** se encarga de servir la aplicación web.

---

## 🛠️ Tecnologías utilizadas

- **Java 17**
- **Spring Boot 3**
- **Thymeleaf**
- **Maven**
- **Docker**
- **Docker Hub**
- **Render**
- **one.com** (DNS)

---

## 📂 Estructura del proyecto

.
├── Dockerfile
├── .dockerignore
├── pom.xml
├── mvnw
├── mvnw.cmd
├── src
│ └── main
│ ├── java
│ │ └── com/ejemplo/tresenraya
│ │ ├── TresEnRayaApplication.java
│ │ └── WebController.java
│ └── resources
│ ├── application.properties
│ └── templates
│ └── index.html


---

## ▶️ Ejecución en local

### Requisitos previos
- Java 17
- Git
- Docker (opcional)

### Ejecución con Maven Wrapper
```bash
./mvnw spring-boot:run
La aplicación estará disponible en:

http://localhost:8080
🐳 Dockerización de la aplicación
La aplicación se ha contenerizado utilizando un Dockerfile multi-stage, lo que permite generar una imagen optimizada y ligera.

Construcción de la imagen Docker
docker build -t gerardocorona/tres-en-raya:1.0 .
Ejecución del contenedor
docker run -p 8080:8080 gerardocorona/tres-en-raya:1.0
📦 Publicación en Docker Hub
La imagen Docker se ha publicado en Docker Hub en el siguiente repositorio:

🔗 Docker Hub
https://hub.docker.com/r/gerardocorona/tres-en-raya

🚀 Despliegue en Render
El despliegue de la aplicación se realizó en Render utilizando la opción Existing Image, enlazando directamente la imagen almacenada en Docker Hub.

Imagen utilizada en Render
docker.io/gerardocorona/tres-en-raya:1.0
Render gestiona automáticamente:

La variable de entorno PORT

El despliegue del contenedor

La disponibilidad pública de la aplicación

🌍 Configuración del dominio personalizado
Se configuró un dominio personalizado para acceder a la aplicación desplegada.

Dominio final
🔗 https://actividadrafa.gerardocorona.io

Proveedor DNS
one.com

Configuración DNS
Se añadió un registro DNS de tipo CNAME:

Tipo	Host	Apunta a
CNAME	actividadrafa	tres-en-raya-1-0.onrender.com
Tras la propagación del DNS, Render verificó el dominio y habilitó HTTPS automáticamente.

🔐 HTTPS
El certificado SSL/TLS fue gestionado automáticamente por Render una vez verificado el dominio personalizado, proporcionando acceso seguro a la aplicación.

🔗 Enlaces importantes
Repositorio del proyecto: (añadir enlace de GitHub)

Docker Hub: https://hub.docker.com/r/gerardocorona/tres-en-raya

Aplicación desplegada: https://actividadrafa.gerardocorona.io

✅ Conclusión
Con esta actividad se ha conseguido:

Crear una aplicación web funcional con Spring Boot

Contenerizar la aplicación mediante Docker

Publicar la imagen Docker en Docker Hub

Desplegar la aplicación en Render utilizando una imagen existente

Configurar un dominio personalizado con HTTPS

Este proceso reproduce un flujo real de despliegue profesional, similar al utilizado en entornos de producción.

