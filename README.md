# make-ai-newsletter

# Automated AI Newsletter Generator (Make + Groq)

Este repositorio contiene el plano de arquitectura (*blueprint*) de una automatización desarrollada en **Make**. El sistema recopila noticias de Inteligencia Artificial mediante canales RSS, procesa y resume la información de forma ejecutiva utilizando el modelo de lenguaje **meta-llama/llama-4-scout-17b-16e-instruct** a través de **Groq**, y distribuye un boletín de noticias optimizado por correo electrónico.

## 🚀 Características del Flujo
- **Extracción Automatizada:** Monitoreo constante de fuentes de noticias de tecnología y optimización mediante nodos RSS.
- **Procesamiento de Lenguaje Natural:** Conexión con la API de Groq para limpiar el ruido del contenido, extraer los puntos clave y formatear de manera consistente.
- **Control de Estructura Dinámica:** Implementación de técnicas avanzadas de *Few-Shot Prompting* directamente en el modelo para forzar una entrega visual limpia (títulos unificados, párrafos consistentes y separaciones simétricas) sin depender de expresiones regulares complejas.
- **Maquetación e Inyección HTML:** Modularización del texto resumido e inyección dinámica dentro de plantillas de diseño estructuradas con CSS nativo.
- **Distribución:** Envío automatizado a través del módulo de Gmail.

## 🛠️ Tecnologías Utilizadas
- **Plataforma de Automatización:** Make
- **Inferencia de IA:** Groq API (Integración con `meta-llama/llama-4-scout-17b-16e-instruct`)
- **Formatos de Intercambio:** JSON, RSS, HTML/CSS

## 📦 Cómo Replicar este Proyecto
Para importar esta automatización en tu propia cuenta de Make, sigue estos pasos:

1. Descarga el archivo `mailai.blueprint.json` que se encuentra en este repositorio.
2. Inicia sesión en tu espacio de trabajo de [Make](https://www.make.com/).
3. Crea un **Nuevo Escenario** (*Create a new scenario*).
4. Selecciona **Import Blueprint**.
5. Carga el archivo `.json` descargado.

### 🔑 Configuración de Credenciales
Para que los módulos funcionen correctamente, deberás asociar tus propias cuentas:
* **Módulo de Groq:** Deberás ingresar a tu consola de desarrollador en Groq, generar una nueva **API Key** y pegarla al crear la conexión en Make. El flujo está configurado específicamente para realizar la inferencia con el modelo `meta-llama/llama-4-scout-17b-16e-instruct`.
* **Módulo de Gmail / RSS:** Otorga los permisos de autenticación estándar correspondientes en tu cuenta de Make.
