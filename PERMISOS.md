## Gestión de Permisos, Licencias y Riesgos

### 1. Permisos y Autorizaciones Necesarias

El uso de tecnologías de terceros y el manejo de datos privados requiere las siguientes autorizaciones:

* **APIs y Servicios:**
* **Firebase (FCM):** Aceptación de los términos de servicio de Google Cloud y configuración de permisos de comunicación en el manifiesto de la app (`AndroidManifest.xml` y `Info.plist`).
* **Tiendas de Aplicaciones:** Registro en Google Play Console / Apple App Store para la distribución (requiere cumplir con normativas de seguridad).


* **Licencias de Software:**
* **Librerías de Cifrado:** Todas las librerias y utilidades utilizadas son de codigo libre y uso gratuito.
* **Docker y PostgreSQL:** Uso bajo licencias de código abierto comerciales/comunitarias.


* **Gestión de Datos:**
* **Cumplimiento Legal:** Al no ofrecer un producto al publico, sino ofrecer el codigo para que cualquier usuario con laguna experiencia en sistemas pueda montarlo para el mismo no debo cumplir ningun tratamiento de datos.


* **Hosting:** Se utiliza el puerto 3815 para el despliege de la API.

### 2. Identificación de Riesgos Técnicos y Organizativos

| Riesgo | Tipo | Descripción |
| --- | --- | --- |
| **Fuga de Claves** | Técnico | Compromiso de las claves privadas en el cliente si no se almacenan en un entorno seguro. |
| **Latencia de Red** | Técnico | Los WebSockets pueden fallar en redes inestables, causando pérdida de mensajes si no hay ACK. |
| **Caducidad de Licencias** | Organizativo | El fin de soporte de una librería crítica de cifrado puede dejar la app vulnerable. |
| **Escalabilidad de Sockets** | Técnico | Un aumento repentino de usuarios puede saturar la memoria del contenedor de Express JS. |

### 3. Plan de Prevención y Medidas Correctoras

Para mitigar los riesgos identificados, se establece el siguiente protocolo:

#### Medidas Preventivas (Proactivas)

* **Almacenamiento Seguro:** Uso obligatorio de `EncryptedStorage` en React Native para las llaves de cifrado.
* **Monitorización:** Implementar logs de Docker para detectar caídas del servicio de base de datos o API en tiempo real.
* **Auditoría de Dependencias:** Uso de comandos como `npm audit` periódicamente para parchear vulnerabilidades en librerías de Node.

#### Medidas Correctoras (Reactivas)

* **Plan de Contingencia ante Caídas:** Si el contenedor Docker falla, el sistema cuenta con un *restart policy* automático (`restart: always`).
* **Backup de Base de Datos:** Ejecución de *dumps* diarios automáticos de PostgreSQL para evitar pérdida de historial de mensajes no entregados.

