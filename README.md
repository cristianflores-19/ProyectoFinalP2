# 📱 ADAPTIA - Fitness App Inteligente

<p align="center">
  <img src="https://img.shields.io/badge/Plataforma-Android-3DDC84?style=for-the-badge&logo=android" alt="Plataforma: Android">
  <img src="https://img.shields.io/badge/Automatización-n8n-FF6838?style=for-the-badge&logo=n8n" alt="Automatización: n8n">
  <img src="https://img.shields.io/badge/Lenguaje-%2FJava-7038FF?style=for-the-badge&" alt="Lenguaje: Java">
</p>
# Videos del proyecto
Cristian Flores: https://drive.google.com/file/d/1DDDxcdkVBIXoBggiLATeXa2rti_jtPjj/view?usp=sharing
Celso Gabriel: https://drive.google.com/file/d/1V1FjHesuyATHYWvL6st_2z5ymH0r6gT1/view?usp=sharing

## ✨ Descripción del Proyecto

**ADAPTIA** es una aplicación **Android** de fitness que ofrece rutinas personalizadas y se distingue por su integración inteligente con **n8n**. Esta herramienta de automatización permite un **sistema de recordatorios por email** y un **sistema de logros por Telegram**, mejorando significativamente la experiencia del usuario, la motivación y la adherencia al ejercicio.

---

## 🚀 Integración con n8n: Automatización Asistida

El núcleo de la funcionalidad avanzada de ADAPTIA reside en el uso de **Webhooks** como puente de comunicación con flujos de trabajo en **n8n**.

### ⚙️ Mecanismo de Comunicación

1.  **Activación desde la App:** La aplicación móvil envía peticiones **HTTP POST** con datos en formato **JSON** (por ejemplo, email del usuario o ID del logro) a *endpoints* específicos.
2.  **Punto de Entrada n8n:** Un **nodo Webhook** actúa como receptor de estas peticiones.
3.  **Procesamiento:** El flujo en n8n procesa automáticamente los datos JSON y ejecuta la acción correspondiente en servicios externos.

| Funcionalidad | Servicio Conectado | Endpoint n8n |
| :--- | :--- | :--- |
| **Recordatorios de Rutina** | Email (Gmail) | Webhook para POST |
| **Notificación de Logros** | Telegram Bot | Webhook para POST |

---

## 🛠️ Requisitos y Dependencias

Para el correcto despliegue y funcionamiento de la integración:

### 📱 Prerrequisitos de la Aplicación Android

| Requisito | Detalle |
| :--- | :--- |
| **IDE** | Android Studio **Arctic Fox** o superior |
| **JDK** | **JDK 11+** |
| **Dispositivo/API** | Dispositivo Android o emulador (**API 21+**) |
| **Permisos** | **`android.permission.INTERNET`** en `AndroidManifest.xml` (crucial para los Webhooks) |

### 🌐 Configuración de n8n (Backend)

* **Credenciales OAuth2:** Necesarias para la conexión segura con **Gmail**.
* **Bot de Telegram:** Token y configuración de un bot para el envío de notificaciones de logros.
* **URLs de Webhooks:** Las URLs específicas y secretas de cada flujo de n8n deben estar configuradas dentro del código de la aplicación Android.

---

## 📦 Pasos de Instalación

Sigue estos pasos para configurar y ejecutar ADAPTIA.

### 1. Clonar el Repositorio

Abre tu terminal y ejecuta:
```bash
git clone (https://github.com/cristianflores-19/ProyectoFinalP2)
