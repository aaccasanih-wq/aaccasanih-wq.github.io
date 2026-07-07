---
layout: project
title: "KAYLA"
subtitle: "Recordatorios automáticos de citas y medicamento para postas de salud."
tag: "Case study · Salud · AI agents (roadmap)"
date: "Junio 2026"
role: "Solo founder · Producto + Ingeniería"
duration: "Course project: Data Science con Python (U. del Pacífico)"
demo: "https://kayla2026.streamlit.app"
repo: "https://github.com/aaccasanih-wq/KAYLA"
video: "https://drive.google.com/file/d/1WlgMcpxPz_G7Xx2B4wihIAoTQczaZimF/view?usp=sharing"
summary: "Sistema que automatiza el recordatorio de citas y recojo de medicamentos para postas de salud peruanas. Hoy ya corre con Google Sheets + un bot de Telegram + dashboard en Streamlit; el roadmap es evolucionar hacia agentes de IA conversacionales (texto y voz)."
---

## TL;DR del producto

> **Problema.** El **39.7 % de pacientes hipertensos peruanos** no se adhiere al tratamiento farmacológico (ENDES 2022). En las postas de primer nivel del MINSA, médicos y enfermeras **pierden horas llamando manualmente** a pacientes para recordarles sus citas y recojos de medicamento. Si no se cumplen las métricas de la Diris/Diresa, la posta pierde recursos.
>
> **Cómo lo resuelven hoy.** Excel + llamadas manuales + WhatsApp personal del médico. Sin sistema, sin automatización, sin métricas.

> **Solución actual (en producción).** Un **Google Form** captura la base de pacientes, alimenta un **Google Sheet**. Cada mañana un **scheduler en GitHub Actions** filtra a quienes tienen fecha próxima (control o recojo de medicamento en 2 días) y envía un **recordatorio automático por Telegram** al médico a cargo. Un **dashboard en Streamlit** permite monitorear el estado de todos los pacientes y recordatorios.
>
> **Roadmap de IA.** El flujo actual es el MVP estable, en uso. El siguiente paso es agregar **agentes de IA conversacionales** (texto y voz) que conversen directamente con el paciente en lugar de solo notificar al médico — aplicando prompting, ingeniería de contexto y RAG.

## Por qué importa este proyecto

KAYLA es exactamente el tipo de producto que querría operar en un equipo de IA: un agente que se comunica con usuarios finales (médicos primero, pacientes después), cuyo éxito se mide con métricas de conversión (adherencia al tratamiento), que requiere **QA continuo sobre los mensajes que envía** y un **dashboard para monitorear el funnel**.

Building it me enseñó los problemas del día a día de un agente IA en producción: fallos en horarios, mensajes que el usuario no entiende, datos incompletos en la base, necesidad de revisión manual de outputs. Es la operativa del rol de Analista de IA en AUNA, aunque a menor escala.

## ¿Cómo funciona hoy (MVP live)

```
┌─────────────────┐     ┌──────────────────┐     ┌─────────────────┐
│  Google Form    │────▶│  Google Sheets   │────▶│  Script Python  │
│  (médico        │     │  (base de datos  │     │  (GitHub Actions│
│   registra)     │     │   de pacientes)  │     │   cada mañana)  │
└─────────────────┘     └──────────────────┘     └────────┬────────┘
                                                          │
                              ┌───────────────────────────┘
                              ▼
                    ┌─────────────────┐
                    │  Telegram Bot   │──▶ Médico recibe:
                    │  (al médico     │    "Juan Pérez (HTA) debe
                    │   a cargo)      │     recoger medicamento
                    │                 │     el 25/06. Cel: 999888777"
                    └─────────────────┘
                              │
                              ▼
                    ┌─────────────────┐     ┌─────────────────┐
                    │  Streamlit       │────▶│  Landing page   │
                    │  (dashboard web  │     │  (GitHub Pages  │
                    │   de métricas)   │     │   con pricing)  │
                    └─────────────────┘     └─────────────────┘
```

### Flujo paso a paso

1. El médico registra pacientes en un **Google Form** (o edita directo el Google Sheet).
2. Cada mañana, el scheduler **GitHub Actions** revisa quién tiene fecha de recojo/control en los próximos 2 días.
3. Envía un mensaje de **Telegram** al médico a cargo con los datos del paciente.
4. El médico contacta al paciente y confirma la asistencia.
5. El **dashboard en Streamlit** muestra el estado de todos los pacientes y recordatorios.

<figure>
  <img src="{{ '/assets/img/kayla-form.png' | relative_url }}" alt="Google Form de registro de pacientes">
  <figcaption>1. El médico registra al paciente en un Google Form accesible desde el celular.</figcaption>
</figure>

<figure>
  <img src="{{ '/assets/img/kayla-sheet.png' | relative_url }}" alt="Google Sheets con base de pacientes">
  <figcaption>2. La base de pacientes se acumula en un Google Sheet (fuente única de verdad).</figcaption>
</figure>

<figure>
  <img src="{{ '/assets/img/kayla-telegram.png' | relative_url }}" alt="Mensaje de Telegram que recibe el médico">
  <figcaption>3. El médico recibe el recordatorio automáticamente en Telegram cada mañana.</figcaption>
</figure>

<figure>
  <img src="{{ '/assets/img/kayla-dashboard.png' | relative_url }}" alt="Dashboard en Streamlit">
  <figcaption>4. El dashboard de Streamlit monitorea en tiempo real el estado de todos los recordatorios y pacientes.</figcaption>
</figure>

## Insight de producto que aprendí

> No es un problema de "falta de tecnología en salud". Es un problema de **herramientas que no llegan al primer nivel**. Las postas no tienen presupuesto para software de gestión, pero **sí tienen Google Sheets y Telegram**. El sistema debe funcionar con lo que ya usan.

Construí KAYLA partiendo de la restricción, no de la utopía: no podemos pedir a una enfermera rural que aprenda un CRM de salud en producción. Pero sí podemos meter un Google Form en su teléfono — y de ahí el sistema hace el resto. Esa es la lección de producto más importante de KAYLA.

## Roadmap de IA

El estado actual **no usa IA**: reglas determinísticas + Python + integraciones. El roadmap es donde entra la IA:

| Plazo | Hito |
|-------|------|
| **3 meses** | 3 postas activas, sistema estable con Telegram, primeros usuarios pagando (plan Pro). |
| **6 meses** | **Agentes de voz con IA** que llaman directamente a los pacientes; dashboard con predicción de abandono. |
| **12 meses** | 50 postas (1 micro-red), expansión a **clínicas privadas** con agentes de IA de voz para reservas y confirmaciones de citas. |

Aplicación concreta de IA en este roadmap:
- **Prompting + RAG** para responder preguntas del paciente sobre su cita / medicamento.
- **Arquitectura de agentes** que deciden si derivan al médico o resuelven solos.
- **QA manual diario** sobre una muestra de conversaciones tal como se hace con cualquier agente IA en producción — la operativa por la que me postulo a AUNA.

## Stack y herramientas

| Capa | Tecnología | Justificación |
|------|-----------|---------------|
| Backend / Script | Python 3.11 | Ecosistema amplio y acceso rápido a APIs. |
| Base de datos | Google Sheets | Los médicos ya lo usan; cero curva de aprendizaje. |
| Ingesta de datos | `gspread` + Google Forms | Lectura/escritura de Sheets desde Python. |
| Mensajería | Telegram Bot API (`python-telegram-bot`) | Gratis, robusto, fácil de configurar. |
| Dashboard | Streamlit | Rápido de construir, desplegable gratis. |
| Landing | HTML/CSS estático + GitHub Pages | Gratis, profesional. |
| Scheduler | GitHub Actions | Gratis (500 min/mes), integrado al repo. |
| Tests | pytest (24 tests), ruff (lint) | Calidad del flujo end-to-end. |
| Asistencia de código | Claude Code | Co-founder de ingeniería virtual. |

## Calidad y operativa (CI/CD + tests)

- **Lint** con `ruff` en cada push y PR hacia `main`.
- **Chequeo de sintaxis** con `python -m py_compile` sobre `backend/` y `frontend/`.
- **24 tests automatizados**: filtrado por fechas, generación de recordatorios, E2E del flujo con mocks (Sheets → filtro → agrupado → Telegram, incluyendo routing por `chat_id` y modo *dry-run*), resolución de credenciales (env JSON, base64, archivo).

Esto me aseguró poder iterar sin romper el flujo productivo — un cambio se mergea solo si pasa todos los tests.

## Validación en terreno

Para no construir sobre supuestos, hice 5 validaciones documentadas en `docs/research/`:

1. Entrevista con médico de posta (#1).
2. Entrevista con médico de posta (#2).
3. Observación de flujo en posta.
4. Validación de métricas del MINSA contra fuentes oficiales (Diris/Diresa).
5. Lista de espera y señales de demanda (tracción temprana).

## Modelo de negocio

**Freemium B2B ligero** (no vendemos al Estado directamente; vendemos a profesionales de salud y operadores de micro-redes que presionan hacia arriba):

| Plan | Precio | Incluye |
|------|--------|---------|
| **Gratis** | S/0/mes | 1 posta, hasta 50 pacientes, recordatorios por Telegram, Google Sheets. |
| **Pro** | S/49/mes | Hasta 3 postas, 500 pacientes, dashboard con métricas, reporte mensual para Diris. |
| **Micro-red** | S/199/mes | 10 postas, pacientes ilimitados, admin centralizado, onboarding personalizado. |

> Costo variable por usuario: ~S/0 (Telegram gratis, Sheets gratis, GitHub Actions gratis). Margen de contribución cercano al 100 %.

## Lo que me enseño KAYLA (learnings)

1. **Producto > tecnología.** El MVP ganó por usar lo que el usuario ya conocía (Sheets + Telegram), no por la tecnología más moderna.
2. **QA de IA es 80 % de operativa, 20 % de glamour.** Cuando un agente falla, casi siempre es porque un dato upstream falla — no porque el modelo sea malo.
3. **Las métricas de conversión en salud son difíciles de atribuir** a un recordatorio (la adherencia depende de muchos factores). Por eso el dashboard mide mucho más: contacto, respuesta al recordatorio, tiempo hasta contacto, etc.
4. **La validación precede al código.** Antes de abrir el editor ya había hecho 5 entrevistas y validado el problema con datos del ENDES 2022.

## Links

- 🔴 **Repo:** [github.com/aaccasanih-wq/KAYLA](https://github.com/aaccasanih-wq/KAYLA)
- 🟢 **Demo (dashboard):** [kayla2026.streamlit.app](https://kayla2026.streamlit.app)
- 🔵 **Landing page:** [aaccasanih-wq.github.io/KAYLA](https://aaccasanih-wq.github.io/KAYLA/)
- 🎬 **Video demo:** [Google Drive](https://drive.google.com/file/d/1WlgMcpxPz_G7Xx2B4wihIAoTQczaZimF/view?usp=sharing)

---

*Course project: Data Science con Python (2026-I), Universidad del Pacífico — Departamento de Economía. Construido con asistencia de Claude Code como co-founder de ingeniería virtual.*