# Microservices Demo – Proyecto Personal

Autor: Arnold Muñoz (ArnoldMunozC)

Descripción
- Este es mi proyecto personal para practicar y demostrar conceptos de arquitectura de microservicios con Java y Spring.
- Incluye buenas prácticas de diseño, documentación, y una guía simple para ejecutar los servicios de forma local.

Objetivos del proyecto
- Diseñar servicios independientes, desplegables de forma autónoma.
- Practicar patrones de integración entre servicios (HTTP/REST) y tolerancia a fallos.
- Preparar el proyecto para observabilidad y despliegue en contenedores.

Tecnologías (stack)
- Java 17+
- Spring Boot / Spring Web
- Spring Cloud (config, discovery, gateway) – opcional según la rama/servicios
- Maven
- Docker y Docker Compose (opcional para despliegue local)

Requisitos previos
- JDK 17 o superior
- Maven 3.9+ (si planeas compilar y ejecutar desde terminal)
- Docker (opcional, solo si usarás contenedores)

Cómo clonar
```
git clone git@github.com-arnold:ArnoldMunozC/microservices.git
cd microservices
```

Compilación
```
mvn clean package -DskipTests
```

Ejecución local (opción A: desde IDE)
- Importa el proyecto como Maven project.
- Ejecuta el/los servicios desde tu IDE (Run/Debug) con el perfil/puerto que desees.

Ejecución local (opción B: desde terminal)
- Para cada servicio (dentro de su carpeta):
```
mvn spring-boot:run
```
—o— si prefieres el .jar:
```
java -jar target/<nombre-del-servicio>-<version>.jar
```

Ejecución con Docker (opcional)
- Si cuentas con Dockerfiles y/o docker-compose.yml:
```
docker compose up --build
```

Comprobaciones rápidas
- Salud del servicio: GET http://localhost:<PUERTO>/actuator/health
- Endpoint de ejemplo (si aplica): GET http://localhost:<PUERTO>/api/...

Estructura (resumen)
- Monorepo con uno o varios servicios. Cada servicio se compila y ejecuta de forma independiente.
- Configuración y composición local documentadas en este README para facilitar el arranque.

Buenas prácticas incluidas/planeadas
- Manejo de configuración por entorno (application-*.yml)
- Perfiles de Spring para desarrollo y producción
- Validaciones y manejo de errores
- Observabilidad (Actuator / métricas) – a integrar
- Contenerización con Docker – a integrar

Roadmap
- Añadir documentación de endpoints (OpenAPI/Swagger)
- Incorporar observabilidad (métricas, tracing y logging centralizado)
- Scripts de despliegue en contenedores (Docker/Compose)
- Tests automatizados y pipeline CI

Contribución
- Sugerencias y PRs son bienvenidos. Este proyecto es principalmente de aprendizaje personal.

Licencia
- MIT

Contacto
- GitHub: https://github.com/ArnoldMunozC
- Email: maomauricioc@gmail.com
