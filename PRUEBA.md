---

# Guía de Prueba del Proyecto

Esta guía permite a cualquier usuario probar la aplicación de mensajería sin necesidad de instalar entornos de desarrollo complejos.

## 1. Acceso al Código Fuente

El proyecto se divide en dos módulos principales alojados en GitHub:

* **Backend (API & Database):** [[Enlace al Repositorio Backend]](https://github.com/JPLY-XYZ/superposition-api-chat)
* **Frontend (App Móvil):** [[Enlace al Repositorio Frontend]](https://github.com/JPLY-XYZ/superposition-chat-react-native)

---

## 2. Instrucciones para el Usuario Final 

Para probar la aplicación móvil de forma inmediata, sigue estos pasos:

### Paso 1: Instalación de la app movil

1. Descarga la aplicación [AQUI](https://github.com/JPLY-XYZ/SUPERPOSITION-CHAT/releases/tag/1.0.3) o escanea el siguiente QR en tu dispositivo móvil.

<img width="341" height="335" alt="image" src="https://github.com/user-attachments/assets/8645fae9-9134-493a-ac66-328f4d52790c" />


#### ***Asegúrate de que tu móvil tenga conexión a internet.***
---

## 3. Instrucciones para Usuarios Técnicos

Si deseas ejecutar toda la infraestructura (incluyendo el servidor) en tu propia máquina:

### Requisitos Previos

* Tener instalado **Docker** y **Docker Compose**.
* Tener instalado **Node.js** (versión LTS).

### Configuración del Backend (Servidor y Base de Datos)

1. Clona el repositorio del backend.
2. En la raíz del proyecto, ejecuta el comando:
```bash
docker-compose up -d

```


*Esto levantará automáticamente la base de datos PostgreSQL y la API de Express.*
3. El servidor estará disponible en `http://localhost:3815`.

### Configuración del Frontend (App Móvil)

1. Clona el repositorio del frontend.
2. Instala las dependencias necesarias:
```bash
npm install

```


3. Inicia el entorno de desarrollo:
```bash
npx expo start

```


4. Sigue las instrucciones en consola para abrir el emulador o conectar tu dispositivo físico.

---

## 4. Recursos Incluidos para la Prueba

Para facilitar la validación, los repositorios incluyen:

* **`.env.example`:** Archivo de ejemplo con las variables de entorno necesarias.
* **`.env.example`:** Script dentro de la carpeta del backend para inicializar las tablas de mensajes y usuarios.

---
