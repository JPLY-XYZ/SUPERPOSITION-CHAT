# Proyecto: App de Mensajería centrada en la seguridad

## Descripción del Proyecto

* **Idea general:** Aplicación de mensajería instantánea multiplataforma (Móvil y Web) centrada en la comunicación en tiempo real.
* **Problema que resuelve:** Proporciona una infraestructura de comunicación robusta y escalable sin la complejidad de gestionar servidores propios, priorizando la entrega fiable de mensajes.
* **Público objetivo:** Usuarios que requieren mensajería rápida y sincronizada entre dispositivos móviles y web.

## Funcionalidades Principales

* **Chat en Tiempo Real:** Mensajería instantánea con sincronización inmediata.
* **Intercambio Multimedia:** Envío y recepción de imágenes y vídeos optimizados.
* **Notificaciones Push Fiables:** Sistema de alertas garantizado incluso con la app cerrada.
* **Soporte Multiplataforma:** Cliente móvil nativo y cliente web sincronizados.

## Tecnologías Utilizadas

| Tecnología | Propósito Específico |
| --- | --- |
| **React Native** | Desarrollo del cliente móvil utilizando JavaScript como lenguaje de programación y librerías de Node. |
| **Next.js** | Desarrollo del cliente web para una interfaz rápida y reactiva utilizando JavaScript como lenguaje de programación y librerías de Node. |
| **Supabase** | Backend como servicio: gestiona la base de datos PostgreSQL, autenticación y eventos *Realtime*. |
| **+Docker** | Herramienta que permite hacer despliegues rápidos y de forma sencilla. |
| **Firebase (FCM)** | Gestión de notificaciones push estándar para asegurar la entrega en segundo plano/app cerrada (Obligatoriamente necesito pasar por Google para la gestión de las notificaciones en Android). |
| **+Cifrado P2P** | Se usarán librerías de Node específicas para el cifrado de extremo a extremo en las conversaciones 1-1. |

## Estado Actual del Proyecto

* **Arquitectura:** Definida y basada en servicios cloud propios en un servidor local, con supabase en un contenedor docker.
* **Notificaciones:** Implementación de librerías de React Native Expo para garantizar la recepción en Android.
* **Desarrollo:** En fase de implementación de funcionalidades básicas en app móvil y migración del backend de Supabase a backend propio.
