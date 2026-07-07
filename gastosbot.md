---
layout: project
title: "GastosBot"
subtitle: "Side project PM: bot de gastos familiares con LLM en lenguaje natural y costo ~$0.05/mes."
tag: "Side project · MVP · LLM · Multi-user"
date: "Mayo 2026"
role: "Builder · Discovery + producto + prompting"
demo: ""
repo: "https://github.com/aaccasanih-wq/gastosbot"
video: ""
summary: "Side project PM end-to-end. Discovery familiar + diseño de dos fuentes de datos (email automática + fallback manual en Telegram) + multi-user desde el día 1 + prompting determinista sobre DeepSeek. Vive 24/7 sin servidor propio y con costo de operación de cinco centavos de dólar al mes."
---

## Resumen

**GastosBot** es un side project PM end-to-end: diseñé el producto desde el discovery (observación de mi propia fricción al registrar gastos de casa) hasta la operativa diaria con LLM en producción. Funciona 24/7 sobre Google Apps Script (sin servidor propio) y combina:

- **Gmail API** para leer notificaciones bancarias entrantes.
- **DeepSeek (LLM)** para extraer monto, concepto, medio de pago y destinatario desde el correo usando prompting.
- **Telegram Bot API** como canal conversacional para consultas y registros manuales (texto o **voz**, transcrita con Groq Whisper).
- **Streamlit** como dashboard de visualización conectado al Google Sheet en tiempo real.

## Problema (discovery)

El control de gastos en casa es un manual de fricciones. Las observé en mí mismo y en mi familia antes de diseñar:

1. **Registrar el gasto** toma tiempo y nadie lo hace de buen grado al terminar de pagar.
2. **Categorizarlo** es aburrido y siempre se retrasa.
3. **Consultar** cuánto se lleva gastado el mes implica abrir el simulador del banco, sumar manualmente, pelearse con la categorización del banco (que casi nunca es útil).
4. Cuando son varios usuarios en casa, los datos terminan repartidos en hojas de Excel inconsistentes.

> **Insight.** El usuario no evita registrar por flojera — evita por fricción. Si eliminas la fricción (no pido nada, leo el correo del banco), capturo el 80 % de los gastos familiares sin esfuerzo.

## Solución (decisión de scope)

Un bot que se conecta a los **correos de notificación bancaria** que el banco ya envía al usuario (BCP, Yape, Interbank). El usuario no tiene que hacer nada nuevo — el dato ya llega.

```
┌────────────────┐    ┌─────────────┐    ┌──────────────┐    ┌─────────────┐
│ Notificaciones │───▶│ Gmail API   │───▶│ Prompting    │───▶│ Google Sheet│
│ del banco      │    │ (cada 1 min)│    │ DeepSeek LLM │    │ (registros)│
└────────────────┘    └─────────────┘    └──────────────┘    └──────┬──────┘
                                                                    │
                            ┌───────────────────────────────────────┘
                            ▼
                  ┌─────────────────────┐
                  │ Dashboard Streamlit │
                  │ Consultas Telegram  │
                  │ (texto o voz)        │
                  └─────────────────────┘
```

### Funciona out-of-the-box para 3 bancos peruanos

- **BCP** (`notificaciones@notificacionesbcp.com.pe`)
- **Yape** (`notificaciones@yape.pe`)
- **Interbank** (`servicioalcliente@netinterbank.com.pe`)

## Decisiones PM documentadas

### 1. Dos fuentes de datos (email + Telegram manual), no una

El correo no cubre efectivo ni Yape entre conocidos. Telegram es la red de seguridad operativa. Si solo tuviera email, perdería el 30–40 % de los gastos reales.**El canal de fallback es tan importante como el canal automatizado.**

### 2. Multi-user desde el día 1

Un solo Sheet de registros no escala a una familia. Pensé en routing por `chat_id` y por sufijo de correo desde el inicio. Si lo hubiera dejado para después, habría tenido que refactor.

### 3. Prompting determinista, no creativo

Para extraer monto y concepto de un correo tuve que escribir prompts con campos estrictos y fallbacks — no "ratio perezoso" de creatividad. **El prompting en producción es el opuesto del prompting en demo.**

### 4. A veces no necesitas un servidor

Apps Script + Sheets + Streamlit Cloud resuelve el 80 % de un producto en cero costo. El constraint empuja el scoping.

### 5. Costo de operación bajo deliberadamente

- **Apps Script**: gratis bajo los límites de Google.
- **DeepSeek API**: < $0.05 USD/mes en uso familiar normal.
- **Groq**: tier gratuito suficiente para voz ocasional.
- **Streamlit Community Cloud**: gratis.
- **GitHub**: repo privado gratis.

**Total:** menos de cinco centavos de dólar al mes. Esto no es side project por hobby — es side project para aprender el costo marginal de un producto en producción.

## Interacción en lenguaje natural

El flujo manual vía Telegram acepta comandos en lenguaje natural — el LLM parsea intención, monto, categoría y operación:

| El usuario escribe… | El bot interpreta |
|---|---|
| *"Gasté 50 soles en almuerzo en efectivo"* | nuevo gasto en cash |
| *"Muéstrame mis últimos 5 gastos"* | listar registros recientes |
| *"¿Cuánto gasté esta semana?"* | total del rango |
| *"¿Cuánto gasté en comida este mes?"* | total por categoría |
| *"Elimina el gasto de ayer en Rappi"* | eliminar por criterio |
| *"Corrige el monto del gasto #42 a 80 soles"* | editar campo |

Acepta **voz** además de texto (transcripción con Groq Whisper).

<figure class="figure-small">
  <img src="{{ '/assets/img/gastosbot-config.png' | relative_url }}" alt="Configuración de usuarios en la hoja Config">
  <figcaption>Hoja <code>Config</code> del Sheet: una fila por usuario, con <code>chat_id</code>, nombre y sufijo de correo de reenvío.</figcaption>
</figure>

<figure class="figure-small">
  <img src="{{ '/assets/img/gastosbot-registros.png' | relative_url }}" alt="Hoja de registros">
  <figcaption>Hoja de registros por usuario — cada pestaña es una persona, con id, fecha, monto, medio, concepto y origen (email/telegram).</figcaption>
</figure>

## Características

- **Multi-usuario.** Una fila en la hoja `Config` por familiar; una pestaña de registros por usuario.
- **Dos fuentes de datos.** Email automático (passive, sin fricción para el usuario) + Telegram manual (cuando se paga en efectivo o no llega notificación).
- **Dashboard interactiva** con gráficos en tiempo real: gasto por mes, distribución por concepto, gasto por medio de pago, evolución diaria, comparación entre familiares, top beneficiarios.

## Lo que me enseñó como PM

1. **El prompting en producción tiene que ser determinista, no creativo.** Para extraer monto y concepto de un correo tuve que escribir prompts con campos estrictos y fallbacks, no "ratio perezoso" de creatividad.
2. **El canal de fallback es tan importante como el canal automatizado.** El correo no cubre efectivo ni los Yape entre conocidos. Telegram es la red de seguridad operativa.
3. **Multi-usuario desde el día 1 cambia la arquitectura.** Una sola hoja de registros no escala a una familia; hay que pensar en routing por `chat_id` y por sufijo de correo desde el inicio.
4. **A veces no necesitas un servidor.** Apps Script + Sheets + Streamlit Cloud resuelve el 80 % de un producto en cero costo.
5. **El costo marginal es una architectural decision.** Elegir Apps Script sobre un backend propio fue un tradeoff explicito por costo marginal ~0 vs. flexibilidad técnica.

## Links

- 🔴 **Repo:** [github.com/aaccasanih-wq/gastosbot](https://github.com/aaccasanih-wq/gastosbot)