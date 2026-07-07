---
layout: default
title: "CV"
description: "CV de Axel Ccasani para roles de Product Manager junior."
---

<div class="cv-page">
  <h1>Axel Aaron Ccasani Huachua</h1>
  <p class="subtitle">Product Manager (junior) · Discovery · MVP IA · Métricas</p>
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
      Economista en formación que construye tres productos de principio a fin con mentalidad PM:
      <strong>discovery antes que código</strong>, scope con tradeoffs explícitos, métricas de funnel,
      roadmap con gateways. He hecho discovery con entrevistas, he diseñado MVPs con y sin desarrollo,
      he definido pricing y medido adopción. Busco mi primer rol formal de PM en un equipo que valore
      product thinking sobre título formal.
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
    <h2>Experiencia</h2>

    <div class="cv-item">
      <div class="cv-item-head"><h3>Practicante de Cuentas por Pagar</h3><span class="date">Nov 2024 – Feb 2025</span></div>
      <div class="cv-item-place">Metso Perú</div>
      <ul>
        <li>Stakeholders: trabajé con el equipo de Cuentas por Pagar y financiero, no técnico. Traduje problemas de proceso en requisitos de herramienta y diseñé una validación en Excel que adoptaron como estándar.</li>
        <li><strong>Tradeoff explícito</strong>: prioricé confiabilidad del dato sobre features más complejas; el resultado fue una reducción de 50 % del tiempo de procesamiento y mejora en la confiabilidad para reportes financieros.</li>
        <li>Tracción: extraje y analicé datos de SAP para monitorear el estado de cuentas por pagar, generando reportes que facilitaron la detección temprana de discrepancias.</li>
        <li>Di seguimiento end-to-end de facturas de principio a fin, gestionando casuísticas y asegurando la trazabilidad de cada resolución hasta el pago — el equivalente a funnel ownership en producto.</li>
      </ul>
    </div>

    <div class="cv-item">
      <div class="cv-item-head"><h3>Practicante de Finanzas</h3><span class="date">Dic 2023 – Abr 2024</span></div>
      <div class="cv-item-place">Nissan Perú</div>
      <ul>
        <li><strong>Discovery cuantitativo</strong>: detecté pagos incorrectos de bonos y descuentos a concesionarios (~20 % del precio base del vehículo) mediante análisis de datos, previniendo fugas de ingresos significantes.</li>
        <li>Diseñé y desarrollé una herramienta de validación en Excel. Tradeoff: simpleza y adopción sobre profundidad técnica — el equipo la adoptó como proceso estándar y el tiempo de validación bajó de 7 a 2 días.</li>
        <li>Realicé análisis cuantitativo de rentabilidad, identificando los factores detrás de la brecha entre ventas proyectadas y reales — un diagnóstico análogo a investigar divergencia entre métricas proyectadas y reales en producto.</li>
        <li>Optimicé procesos internos de control financiero, mejorando la eficiencia operativa del departamento.</li>
      </ul>
    </div>
  </div>

  <div class="cv-section">
    <h2>Proyectos (case studies de producto)</h2>

    <div class="cv-item">
      <div class="cv-item-head">
        <h3>UPLearn — Case study PM: discovery + MVP + modelo de negocio</h3>
        <span class="date">Curso universitario</span>
      </div>
      <div class="cv-item-place">Universidad del Pacífico · <a href="{{ '/uplearn/' | relative_url }}">ver case study completo →</a></div>
      <ul>
        <li><strong>Discovery end-to-end</strong>: framing del reto, mapa de stakeholders, empathy map y research con sesgos cognitivos (cognitive load theory + availability bias) para llegar a un insight de producto accionable.</li>
        <li><strong>Scope tradeoff explícito</strong>: recorté marketplace e-commerce a canal publicitario para reducir complejidad operativa. Decisión documentada — aprendí que el rol del PM en un proyecto es definir qué NO construir.</li>
        <li><strong>Revenue model sostenible</strong>: comisión 15 % sobre tutorías + publicidad no intrusiva. Sin depender de donantes.</li>
        <li><strong>KPIs definidos</strong>: registro, activos, matches tutor–estudiante, % info útil encontrada, deadlines no perdidos, NPS, retención.</li>
      </ul>
    </div>

    <div class="cv-item">
      <div class="cv-item-head">
        <h3>KAYLA — Producto 0→1 en salud con roadmap IA</h3>
        <span class="date">Jun 2026</span>
      </div>
      <div class="cv-item-place">
        <a href="https://github.com/aaccasanih-wq/KAYLA" target="_blank" rel="noopener">github.com/aaccasanih-wq/KAYLA</a> ·
        <a href="https://kayla2026.streamlit.app" target="_blank" rel="noopener">Demo</a> ·
        <a href="{{ '/kayla/' | relative_url }}">case study →</a>
      </div>
      <ul>
        <li><strong>Discovery con evidencia</strong>: 5 entrevistas con médicos de posta + dato ENDES 2022 (39.7 % no adherencia al tratamiento) antes de tocar el editor.</li>
        <li><strong>Scoping por restricción del usuario</strong>: la posta no tiene presupuesto para software de gestión, pero sí tiene Sheets y Telegram. Diseñé a partir de la restricción, no a pesar de ella.</li>
        <li><strong>Pricing y modelo de negocio</strong>: freemium B2B ligero, 3 planes, costo variable ~S/0.</li>
        <li><strong>Roadmap con gateway explícito</strong>: el MVP deterministico actual es estable en producción; el salto a agentes IA es un milestone con justificación, no una feature impulsiva.</li>
      </ul>
    </div>

    <div class="cv-item">
      <div class="cv-item-head">
        <h3>GastosBot — Side project PM con LLM en producción</h3>
        <span class="date">May 2026</span>
      </div>
      <div class="cv-item-place">
        <a href="https://github.com/aaccasanih-wq/gastosbot" target="_blank" rel="noopener">github.com/aaccasanih-wq/gastosbot</a> ·
        <a href="{{ '/gastosbot/' | relative_url }}">case study →</a>
      </div>
      <ul>
        <li><strong>Dos fuentes de datos por diseño</strong>: email automática (passive) + Telegram manual (fallback). El canal de fallback es tan importante como el automatizado — sin él perdería 30–40 % de los gastos familiares.</li>
        <li><strong>Multi-user desde el día 1</strong>: routing por chat_id y por sufijo de correo desde la arquitectura inicial — no refactor posterior.</li>
        <li><strong>Prompting determinista</strong>: campos estrictos y fallbacks, no creatividad libre. Aprendí que prompting en producción es el opuesto del prompting en demo.</li>
        <li><strong>Costo marginal ~$0.05/mes</strong>: Apps Script + Sheets + Streamlit Cloud — el costo marginal como architectural decision.</li>
      </ul>
    </div>

    <div class="cv-item">
      <div class="cv-item-head">
        <h3>AI personal agent</h3>
        <span class="date">Jun 2026</span>
      </div>
      <ul>
        <li>Desarrollé un agente IA basado en DeepSeek (LLM) que procesa voz y texto para gestionar correos, archivos locales y recordatorios, mediante prompting e ingeniería de contexto según la intención del usuario.</li>
        <li>Diseñé una arquitectura extensible tipo módulos, donde cada herramienta es un script autónomo; implementé recuperación de memorias pasadas mediante RAG (retrieval-augmented generation).</li>
        <li>Validé manualmente la precisión y consistencia de las respuestas generadas por el modelo — un proceso equivalente a control de calidad (QA) sobre outputs de IA.</li>
      </ul>
    </div>
  </div>

  <div class="cv-section">
    <h2>Skills PM</h2>
    <div class="cv-skills-grid">
      <div class="cv-skill">
        <h4>Producto</h4>
        <p>Discovery, stakeholder mapping, empathy map, MVP scoping, tradeoff documentation, pricing &amp; revenue model, roadmap with gateways.</p>
      </div>
      <div class="cv-skill">
        <h4>Métricas &amp; analítica</h4>
        <p>Funnel, KPIs, retention, NPS, conversion analysis, A/B thinking, dashboards (Streamlit, Excel, Looker-style).</p>
      </div>
      <div class="cv-skill">
        <h4>IA aplicada</h4>
        <p>Prompting determinista, RAG, fundamentos de arquitectura de agentes, QA de outputs IA, Claude / Gemini / ChatGPT para análisis.</p>
      </div>
      <div class="cv-skill">
        <h4>Técnico</h4>
        <p>Python (Pandas, NumPy, Requests, Selenium, Langchain), SQL, R, Excel intermedio-avanzado, Google Apps Script, GitHub Actions.</p>
      </div>
      <div class="cv-skill">
        <h4>Soft skills</h4>
        <p>Comunicación con stakeholders no técnicos, documentación de decisiones, negociación de requirements, escritura para convencer.</p>
      </div>
      <div class="cv-skill">
        <h4>Idiomas</h4>
        <p>Español (nativo), Inglés (avanzado).</p>
      </div>
    </div>
  </div>

  <div class="cv-section">
    <h2>Filosofía de producto</h2>
    <p style="color:var(--text-mute); font-style: italic;">
      "Producto que el usuario realmente usa — no producto que se ve bien en demo."
      Discovery precede al código. El scope se define por lo que NO se construye. El prompting en producción es determinista, no creativo. El canal de fallback es tan importante como el canal automatizado. El costo marginal es una architectural decision.
    </p>
  </div>
</div>