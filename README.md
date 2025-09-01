# Agente IA de Huella Digital y Perfilado Automatizado

## Resumen del Proyecto

Este Trabajo de Fin de Máster (TFM) presenta el desarrollo de un sistema automatizado para la obtención y análisis de la huella digital y el perfilado de entidades, integrando plataformas modernas como N8N, OpenWebUI, MCP Servers y diversas APIs OSINT. El objetivo es centralizar, normalizar y exponer información de múltiples fuentes para facilitar su procesamiento por sistemas de inteligencia artificial.

## Arquitectura Modular

La solución se basa en una arquitectura orquestada por N8N, que automatiza la recopilación, procesamiento y correlación de datos. El flujo principal se compone de los siguientes módulos:

- **Entrada (Input):** Recepción de datos vía Webhook, MCP o Telegram.
- **Autenticación:** Verificación de usuarios y gestión de suscripciones mediante Stripe.
- **Agente IA:** Orquestador que decide qué herramientas y APIs utilizar, accediendo a la memoria contextual.
- **Herramientas:** APIs especializadas para búsqueda de datos, brechas, reconocimiento facial, etc.
- **Memoria:** Almacenamiento de contexto y resultados intermedios.
- **Validador:** Normalización y control de calidad de los resultados.
- **Salida (Output):** Generación de informes y presentación de resultados.

## Uso del Agente

El agente desarrollado puede utilizarse desde diferentes plataformas y admite múltiples formas de interacción para adaptarse a las necesidades de los usuarios:

### Plataformas Disponibles

- **OpenWebUI:** Interfaz web moderna que permite la interacción directa con el agente, envío de texto e imágenes, y visualización de resultados de forma estructurada.
- **Clientes MCP:** El sistema puede funcionar como servidor MCP, permitiendo su integración como subagente en otros sistemas LLM y facilitando su uso desde herramientas como Claude, ChatGPT o Cursor.
- **Bot de Telegram:** Acceso sencillo y rápido desde dispositivos móviles, permitiendo consultas OSINT y perfilado desde la aplicación de mensajería.

### Formas de Interacción

El agente admite entradas variadas:
- **Texto:** Números de teléfono, correos electrónicos, nombres de usuario, alias, etc.
- **Imágenes:** Para búsquedas de reconocimiento facial inverso.

Las entradas pueden proporcionarse manualmente o recibirse automáticamente desde otras aplicaciones o servicios, lo que otorga gran flexibilidad.

### Generación de Informes

Tras el análisis, el sistema genera informes estructurados que incluyen:
- Resumen general de la información encontrada.
- Datos concretos (emails, usuarios, teléfonos, etc.).
- Análisis psicológico (si hay suficiente información).
- Registro de herramientas utilizadas y datos encontrados.
- Sugerencias de acción para el usuario.
- Gráficos, tablas y enlaces a fuentes originales.

Estos informes pueden visualizarse en la interfaz web o exportarse para su uso en otros contextos.

## Plataformas y Herramientas Utilizadas

- **N8N:** Backend de automatización de workflows.
- **OpenWebUI:** Interfaz de usuario moderna para interacción y visualización.
- **MCP Servers:** Permite la integración como subagente en otros sistemas LLM.
- **APIs OSINT:** TrueCaller, WhatsApp Data, LeakOSINT, Breach Directory, FaceCheck.ID, entre otras.
- **RapidAPI:** Centralización y gestión de acceso a múltiples APIs.
- **OpenRouter:** Acceso a modelos LLM para análisis avanzado.
- **Stripe:** Plataforma para el cobro y administración de suscripciones

## Costes y Modelo de Negocio

El coste operativo mensual estimado es de 100 €/mes, incluyendo infraestructura y consumo de APIs. Se propone un modelo de suscripción de 15 €/mes por usuario, siendo rentable a partir de 7 usuarios activos. El reconocimiento facial es el componente más costoso, por lo que se recomienda limitar su uso.

## Limitaciones y Futuras Mejoras

- Dependencia de APIs externas y sus condiciones.
- Coste elevado de búsquedas faciales.
- Necesidad de mejorar la normalización y correlación de datos.
- Refuerzo de mecanismos de privacidad y cumplimiento legal.
- Potenciar la automatización de informes y visualizaciones interactivas.

## Conclusión

La integración de plataformas de automatización, interfaces modernas y APIs especializadas permite construir sistemas robustos y adaptables para el análisis avanzado de la huella digital y el perfilado automatizado. El enfoque modular facilita la escalabilidad y la incorporación de nuevas capacidades, posicionando la solución como referencia en ciberinteligencia aplicada.

---

**Bot de Telegram** https://t.me/OSINT_RG_Bot



