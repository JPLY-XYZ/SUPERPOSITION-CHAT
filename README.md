# Proyecto: App de Mensajería centrada en la seguridad

## Descripción del Proyecto

* **Idea general:** Aplicación de mensajería instantánea multiplataforma (Móvil y API) centrada en la comunicación en tiempo real.
* **Problema que resuelve:** Proporciona una infraestructura de comunicación escalable sin la complejidad de gestionar servidores propios, priorizando la entrega fiable de mensajes.
* **Público objetivo:** Usuarios que requieren mensajería rápida y segura.

## Funcionalidades Principales

* **Chat en Tiempo Real:** Mensajería instantánea con sincronización inmediata.
* **Intercambio Multimedia:** Envío y recepción de imágenes y vídeos optimizados (No Implementado actualmente).
* **Notificaciones Push Fiables:** Sistema de alertas garantizado incluso con la app cerrada.

## Tecnologías Utilizadas

| Tecnología | Propósito Específico |
| --- | --- |
| **React Native** | Desarrollo del cliente móvil utilizando JavaScript como lenguaje de programación y librerías de Node. |
| **Express JS** | Backend propio: gestiona la base de datos PostgreSQL, autenticación y eventos *Realtime*. |
| **Docker** | Herramienta que permite hacer despliegues rápidos y de forma sencilla. |
| **Firebase (FCM)** | Gestión de notificaciones push estándar para asegurar la entrega en segundo plano/app cerrada. |
| **Cifrado P2P** | Se usarán librerías de Node específicas para el cifrado de extremo a extremo en las conversaciones 1-1. (No Implementado actualmente) |

## Estado Actual del Proyecto

* **Arquitectura:** Definida y basada en servicios cloud propios en un servidor local, con la API en un contenedor docker.
* **Notificaciones:** Implementación de librerías de React Native Expo para garantizar la recepción en Android.
* **Desarrollo:** Fase de ampliación y implementación de tecnologias de cifrado.
