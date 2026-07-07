---
layout: default
title: "CV"
description: "CV de Axel Ccasani — analista de datos e IA. Experiencia, proyectos y skills."
---

<div class="cv-page">
  <h1>Axel Aaron Ccasani Huachua</h1>
  <p class="subtitle">Analista de IA · Data &amp; AI Analytics · Business Intelligence</p>
  <p style="color:var(--text-mute); margin-bottom:24px;">
    +51 986 531 450 ·
    <a href="https://github.com/{{ site.github_username }}" target="_blank" rel="noopener">github.com/{{ site.github_username }}</a> ·
    <a href="mailto:{{ site.email }}">{{ site.email }}</a> ·
    Lima, Perú · DNI 73353714
  </p>

  <div class="cv-actions">
    <a href="{{ '/assets/files/Axel_Ccasani_CV_espanol.pdf' | relative_url }}" target="_blank" class="btn btn-primary">Descargar CV (PDF · español)</a>
    <a href="{{ '/assets/files/Axel_Ccasani_CV.pdf' | relative_url }}" target="_blank" class="btn btn-ghost">CV (PDF · inglés)</a>
  </div>

  <div class="cv-section">
    <h2>Resumen</h2>
    <p style="color:var(--text-mute);">
      Economista en formación con experiencia en automatización de procesos financieros, análisis de datos y proyectos
      de IA aplicada. Fundación sólida en prompting, RAG y arquitectura de agentes IA. Especial interés en roles que
      combinen <strong>QA de IA, seguimiento de métricas de conversión y producto</strong>.
    </p>
  </div>

  <div class="cv-section">
    <h2>Educación</h2>
    <div class="cv-item">
      <div class="cv-item-head"><h3>Lic. en Economía</h3><span class="date">2021 – 2026</span></div>
      <div class="cv-item-place">Universidad del Pacífico · Lima, Perú</div>
      <p style="color:var(--text-mute); font-size:14px;">En proceso de obtener el grado de Bachiller (julio 2026).</p>
    </div>
  </div>

  <div class="cv-section">
    <h2>Experiencia laboral</h2>

    <div class="cv-item">
      <div class="cv-item-head"><h3>Practicante de Cuentas por Pagar</h3><span class="date">Nov 2024 – Feb 2025</span></div>
      <div class="cv-item-place">Metso Perú</div>
      <ul>
        <li>Identifiqué inconsistencias recurrentes en la validación de facturas; diseñé una automatización en Excel que redujo errores y el tiempo de procesamiento en 50%, mejorando la confiabilidad del dato.</li>
        <li>Extraje y analicé datos de SAP para monitorear el estado de cuentas por pagar, generando reportes que facilitaron la detección temprana de discrepancias.</li>
        <li>Di seguimiento de facturas de principio a fin, gestionando casuísticas y asegurando la trazabilidad de cada resolución hasta el pago.</li>
      </ul>
    </div>

    <div class="cv-item">
      <div class="cv-item-head"><h3>Practicante de Finanzas</h3><span class="date">Dic 2023 – Abr 2024</span></div>
      <div class="cv-item-place">Nissan Perú</div>
      <ul>
        <li>Detecté pagos incorrectos de bonos y descuentos a concesionarios (~20% del precio base del vehículo) mediante análisis de datos, previniendo pérdidas de ingresos significativas.</li>
        <li>Diseñé y desarrollé una herramienta de validación en Excel, adoptada como proceso estándar del equipo, reduciendo el tiempo de validación de 7 a 2 días.</li>
        <li>Realicé análisis cuantitativo de rentabilidad, identificando los factores detrás de la brecha entre ventas proyectadas y reales.</li>
        <li>Optimicé procesos internos de control financiero, mejorando la eficiencia operativa del departamento.</li>
      </ul>
    </div>
  </div>

  <div class="cv-section">
    <h2>Proyectos</h2>

    <div class="cv-item">
      <div class="cv-item-head">
        <h3>KAYLA — Recordatorios automáticos para postas de salud</h3>
        <span class="date">Jun 2026</span>
      </div>
      <div class="cv-item-place">
        <a href="https://github.com/aaccasanih-wq/KAYLA" target="_blank" rel="noopener">github.com/aaccasanih-wq/KAYLA</a> ·
        <a href="https://kayla2026.streamlit.app" target="_blank" rel="noopener">Demo</a>
      </div>
      <ul>
        <li>Diseñé un sistema que automatiza recordatorios de citas y de recojo de medicamentos para postas de salud: un Google Form alimenta la base de pacientes en Google Sheets, y un scheduler en GitHub Actions detecta a quienes tienen fecha próxima y envía recordatorios automáticos vía bot de Telegram al médico a cargo.</li>
        <li>Construí un dashboard en Streamlit que consume la base de pacientes y monitorea en tiempo real el estado de cada recordatorio y paciente — equivalente al seguimiento de métricas de un funnel de conversión.</li>
        <li>Definí el roadmap de evolución del producto hacia agentes de IA conversacionales (texto y voz) sobre el flujo actual, aplicando fundamentos de prompting, arquitectura de agentes y RAG; sustenté el caso de uso con evidencia (ENDES 2022: 39.7 % de no adherencia) y 5 entrevistas de validación con médicos de posta.</li>
        <li>Implementé CI/CD con GitHub Actions y tests automatizados (pytest, 24 tests), asegurando la trazabilidad de cambios y la calidad del flujo end-to-end.</li>
      </ul>
    </div>

    <div class="cv-item">
      <div class="cv-item-head">
        <h3>Rastreador de Gastos Automatizado con IA</h3>
        <span class="date">May 2026</span>
      </div>
      <div class="cv-item-place">
        <a href="https://github.com/aaccasanih-wq/gastosbot" target="_blank" rel="noopener">github.com/aaccasanih-wq/gastosbot</a>
      </div>
      <ul>
        <li>Desarrollé una automatización que analiza correos de notificación bancaria vía API de Gmail y utiliza prompting sobre un LLM (DeepSeek) para extracción de lenguaje natural, registrando transacciones automáticamente en Google Sheets.</li>
        <li>Diseñé un flujo complementario vía bot de Telegram (texto o audio) para registro manual, cubriendo casos donde la automatización no aplica — priorizando cobertura de escenarios de uso.</li>
        <li>Construí un dashboard interactivo en Streamlit para el seguimiento de métricas de gasto en tiempo real por categoría, similar al monitoreo de KPIs de un funnel.</li>
      </ul>
    </div>

    <div class="cv-item">
      <div class="cv-item-head">
        <h3>AI personal agent</h3>
        <span class="date">Jun 2026</span>
      </div>
      <ul>
        <li>Desarrollé un asistente de IA basado en DeepSeek (LLM) que procesa voz y texto para gestionar correos, archivos locales y recordatorios, mediante prompting e ingeniería de contexto según la intención del usuario.</li>
        <li>Diseñé una arquitectura extensible tipo módulos, donde cada herramienta es un script autónomo; implementé recuperación de memorias pasadas mediante RAG (retrieval-augmented generation).</li>
        <li>Validé manualmente la precisión y consistencia de las respuestas generadas por el modelo frente a los resultados esperados — un proceso equivalente a control de calidad (QA) sobre outputs de IA.</li>
      </ul>
    </div>
  </div>

  <div class="cv-section">
    <h2>Habilidades &amp; herramientas</h2>
    <div class="cv-skills-grid">
      <div class="cv-skill">
        <h4>Inteligencia Artificial</h4>
        <p>Prompting y análisis de datos con LLM (DeepSeek, ChatGPT, Claude, Gemini), RAG, fundamentos de arquitectura de agentes de IA.</p>
      </div>
      <div class="cv-skill">
        <h4>Programación</h4>
        <p>Python (Pandas, NumPy, Requests, Selenium, Langchain), SQL, R (RStudio), Excel (intermedio-avanzado).</p>
      </div>
      <div class="cv-skill">
        <h4>Análisis de datos</h4>
        <p>Web scraping, limpieza y transformación de datos, análisis estadístico, dashboards, seguimiento de métricas y funnels.</p>
      </div>
      <div class="cv-skill">
        <h4>Finance &amp; BI</h4>
        <p>Análisis de estados financieros, análisis de rentabilidad, diseño de dashboards e informes de gestión.</p>
      </div>
      <div class="cv-skill">
        <h4>Idiomas</h4>
        <p>Español (nativo), Inglés (avanzado).</p>
      </div>
    </div>
  </div>
</div>