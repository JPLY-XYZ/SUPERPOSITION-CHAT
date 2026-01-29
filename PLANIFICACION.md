## Plan de Ejecución Técnica

### 1. Secuenciación de Tareas

El orden de implementación sigue una lógica de dependencia, desde la infraestructura base hasta la capa de seguridad final.

1. **Infraestructura Base:**
* Configuración de **Docker Compose** (Contenedores para Node.js y PostgreSQL).
* Definición del esquema de base de datos en **Prisma ORM**.


2. **Backend Core:**
* Implementación de API REST con **Express** (Registro/Login con JWT).
* Integración de WebSockets usando la libreria **Socket.IO** para el **Realtime**.


3. **Cliente Móvil (MVP):**
* Estructura básica en **React Native**.
* Base de datos local **SQLITE** para trabajar en **offline**
* Conexión al socket y flujo de envío/recepción de mensajes.


4. **Sistema de Notificaciones:**
* Configuración de **Firebase (FCM)** en el backend.


5. **Capa de Seguridad (Fase actual):**
* Integración de librerías criptográficas (Ej: `crypto-js` o `libsignal`).
* Intercambio de claves públicas entre clientes.


6. **Multimedia y Optimización:**
* Gestión de almacenamiento de archivos y optimización de carga.


---

### 2. Procedimientos de Ejecución

#### Desarrollo

* **Versionado:** Uso de Git con 2 proyectos separados.
* **Entorno:** Se hacian pruebas en local, y un despliege final de la api.
* **Documentación:** Registro de endpoints en un archivo de colección (tipo Postman o Insomnia).

#### Pruebas (Testing)

* **Funcionamiento:** Se han realizado pruebas de sincronizacion en entornos controlados para simular interferencias en la red.

#### Despliegue (Deployment)

* **Contenedores:** Generación de imágenes Docker optimizadas.
* **CI/CD:** Automatización básica para el despliegue de la API en el servidor local.
* **Móvil:** Generación de builds de desarrollo a través de Expo Application Services (EAS) para pruebas rápidas.

---
