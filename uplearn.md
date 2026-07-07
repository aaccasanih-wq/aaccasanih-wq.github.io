---
layout: project
title: "UPLearn"
subtitle: "De un reto de división social a un MVP con modelo de negocio — case study PM end-to-end."
tag: "Case study PM · Discovery · MVP · Business model"
date: "Curso universitario · Universidad del Pacífico"
role: "Co-fundador · Discovery + Research + Diseño de producto"
duration: "Trabajo en equipo — curso de innovación social"
demo: ""
repo: ""
video: ""
summary: "Case study completo de un producto universitario desde el reto hasta el modelo de negocio. UPLearn busca democratizar el acceso a material académico, reseñas de profesores y tutorías peer-to-peer dentro de la UP. Documenté discovery (stakeholders, empathy map, insights con sesgos cognitivos), MVP scoping con tradeoffs explícitos y revenue model sostenible."
---

> **Mi rol.** Co-fundador del proyecto en un equipo multidisciplinario. Mi contribución principal fue el **product thinking end-to-end**: framing del reto, mapa de stakeholders, empathy map, research con sesgos cognitivos (cognitive load + availability bias), insights, MVP scoping y revenue model. El MVP fue prototipado en Google AI Studio.

## 1. Cómo llegué al problema (discovery)

Partimos de un framework de "divisiones profundas" que limitan el desarrollo humano sostenible. Nuestro caso se enmarca en dos de ellas:

- **División social** — falta de comunidad, información y apoyo para algunos estudiantes.
- **División espiritual** — presión social e inseguridades ocultas.

> **Reto.** *How might we design a centralized, user-friendly website tailored specifically for the unique culture of the UP, where notes and strategic advice can be shared by students to help all the community?*

No fue un problema inventado en una sala. Yo mismo, como estudiante UP, viví la fragmentación. La observación empírica y las entrevistas con pares vinieron antes que el MVP en Figma.

## 2. Mapa de actores (stakeholder analysis)

| Actor | Involucramiento | Qué busca / aporta |
|---|---|---|
| **Universidad (UP)** | Más involucrado | Estudiantes 1°–5° año que buscan info y consejos; bachelors que venden asesorías; organizaciones que pueden recomendar la plataforma. Alineación con valores y cultura UP. |
| **Sociedad UP** | Más involucrado | Comunidad de estudiantes que comparten info y experiencias. Para el MVP basta con la sociedad UP. |
| **Empresa** | Parcial | Estudiantes/bachelors emprendedores que pagan por publicidad de sus negocios dentro de la plataforma. Software company externa para construir el MVP. |
| **Gobierno** | Menos | Registro de la empresa, impuestos, inspecciones. |

**Decisión de scope.** Para el MVP los stakeholders críticos son solo dos (Universidad y sociedad UP). Gobierno y empresa son posteriores — hacer MVP para los cuatro habría sido scoping defectuoso.

## 3. Empathy map (estudiantes UP)

| Pienso y siento | Veo |
|---|---|
| Quiere la mayor info posible antes de decidir academics. | Info académica dispersa en WhatsApp, Facebook y amigos. |
| No quiere perder el semestre, pasar todo con buenas notas. | Algunos profesores tienen muchas reseñas; otros casi ninguna. |
| Le preocupa perder oportunidades valiosas. | Siente que no hay tiempo y la info de algunas materias no es clara. |

| Digo y hago | Escucho |
|---|---|
| Pido materiales y recomendaciones a amigos. | "Quisiera más info para estudiar mejor, tengo miedo a los exámenes." |
| Uso grupos de FB y WhatsApp para recolectar info. | Amigos y compañeros de clase. |
| Busco recursos más allá de Blackboard. | Estudiantes de ciclos superiores con experiencia. |
| Comparto materiales con amigos cuando me los piden. | |

## 4. Insights (research findings)

Investigación basada en experiencia empírica como estudiante UP, entrevistas personales y frameworks académicos.

### 4.1 La barrera social y el acceso democrático

El éxito académico y el bienestar mental de los estudiantes más comprometidos en la UP dependen **fuertemente del capital social privado**. Estudiantes con amigos en ciclos superiores o en el círculo correcto tienen ventaja significativa.

> Cuando una institución **carece de una plataforma centralizada y abierta**, este capital queda **secuestrado en círculos privados**, perjudicando a estudiantes con menos acceso social, **independientemente de su capacidad intelectual**.

### 4.2 Cultura colaborativa sin sistema democrático

El estudiante promedio UP está dispuesto a compartir materiales cuando se le pide — pero **no tiene un espacio que continuamente fomente y facilite este comportamiento**.

> La barrera para un campus inclusivo **no es la falta de empatía estudiantil**, sino la **falta de un sistema democrático**. Sin un espacio centralizado y abierto, la sabiduría estudiantil queda encerrada en redes privadas — y lo que debería ser apoyo se convierte en activo accidental para unos pocos.

### 4.3 Ecosistema fragmentado gatilla sesgos cognitivos

Los estudiantes enfrentan severas dificultades para obtener respuestas específicas sin tiempo crítico para navegar múltiples chats, drives y grupos. Impulsados por el deadline, suelen recurrir a una **única fuente no verificada**.

De acuerdo a la **cognitive load theory**, el alto estrés pre-examen y navegar un entorno digital caótico causa fatiga y gatilla **availability bias** — el cerebro confía ciegamente en el primer consejo que encuentra porque es accesible, ignorando el riesgo de inexactitud.

> El estudiante **no toma malas decisiones por irresponsable**. Lo hace porque el ecosistema fragmentado **afecta negativamente su decisión**. Si encontrar una reseña confiable y multi-perspectiva toma horas, arriesgar el ciclo en una fuente no verificada se vuelve racional por pánico.

**Insight de producto.** El problema no era "falta de información" — era "falta de un espacio centralizado confiable". Eso reframea el MVP: no necesitabamos crear contenido, necesitábamos agregar contenido existente en un solo lugar con calidad controlada por la comunidad.

## 5. Solución propuesta (scope decisions)

Plataforma exclusiva para la comunidad UP que centraliza:

- **Materiales académicos** — apuntes, resúmenes, exámenes pasados, ejercicios resueltos
- **Reseñas y recomendaciones** de cursos y profesores
- **Insights estratégicos** sobre rutas académicas y profesionales
- **Tutorías peer-to-peer** por estudiantes UP experimentados

> **Por qué una plataforma exclusiva UP y no abierta:** escala más lento, pero la exclusividad (email institucional) es lo que hace confiable el contenido. Sin confianza, el contenido se contamina y el insight del ecosistema fragmentado se repite.

## 6. MVP — UPLearn

MVP llamado **UPLearn**, web diseñada exclusivamente para estudiantes UP. Prototipado navegable, con autenticación simulada con correo institucional y seis secciones funcionales.

### 6.1 Funcionalidades principales

#### 6.1.1 Autenticación estudiantil
Acceso por login con **autenticación simulada restringida a correos institucionales UP** (`@up.edu.pe`). Donde nace la confianza — sin UP email, no hay acceso.

#### 6.1.2 Dashboard
Página principal de la plataforma, que muestra:

- Estadísticas resumen de materiales, reviews y tutores disponibles.
- Recursos académicos cargados recientemente.
- Tutorías destacadas.
- **Negocios estudiantiles patrocinadores** (publicidad no intrusiva).
- Accesos rápidos a las secciones.

> El dashboard **mata dos pájaros de un tiro**: da visibilidad al contenido más relevante para los estudiantes y al mismo tiempo abre un canal de visibilidad para emprendedores universitarios — publicitado de forma no intrusiva.

#### 6.1.3 Materiales académicos
Recursos organizados por curso:

- Apuntes de clase
- Resúmenes de readings
- Ejercicios resueltos
- Exámenes pasados
- Prácticas

Con **búsqueda y filtros** para facilitar acceso a lo relevante. Sin esto, hay clics de más — fricción.

#### 6.1.4 Reviews e insights
Reseñas y recomendaciones compartidas por estudiantes sobre:

- Cursos
- Profesores
- Rutas académicas y profesionales
- Vida universitaria

> Sección diseñada para **reducir la asimetría de información** que identificamos en el insight 4.3. Sin reseñas, el estudiante vuelve a depender de una sola fuente — y vuelve el availability bias.

#### 6.1.5 Tutoring
Conecta estudiantes que buscan apoyo académico con estudiantes que ya completaron exitosamente el curso.

Perfiles de tutor muestran: nombre, áreas de expertise, **rating y reseñas**, tarifa por hora y disponibilidad.

- Reserva de sesiones y **pago directamente por la web**.

> Esta sección es el **motor de monetización** del MVP. Las otras funcionalidades son el hook que justifica entrar; el tutoring es donde la plataforma cobra.

#### 6.1.6 Student businesses
Sección para emprendedores estudiantiles que promocionan productos y servicios. **No funciona como marketplace e-commerce sino como canal**: al hacer click, se redirige a los canales de contacto del emprendedor (web, Instagram, WhatsApp).

> **Tradeoff explícito.** En el case study nos tentamos con marketplace e-commerce (comisión por transacción). Lo recortamos a canal publicitario: reduce complejidad operativa (no gestionamos cobros ni disputas), mantiene un revenue stream y los emprendedores ganan visibilidad sin UX intrusiva. Less is more.

#### 6.1.7 Perfil de usuario
Vista personalizada de la actividad: información del estudiante, materiales cargados, sesiones agendadas y recursos guardados.

> El perfil **premia la participación y las contribuciones** a la comunidad académica — alineado con la cultura colaborativa que identificamos en el insight 4.2.

## 7. Modelo de negocio

### 7.1 Propósito social

> Reducir las brechas de información académica dentro de la Universidad del Pacífico centralizando recursos, oportunidades y apoyo peer-to-peer.

**Problema:** No existen canales de comunicación para compartir información o resolver dudas rápidamente. En cursos pesados (ej. proyecto final de carrera), no hay canales para conectar con especialistas del área.

**Segmentos de cliente:**

- **Jóvenes 18–24 años de todos los ciclos** que necesitan apoyo académico.
- **Early customers:** estudiantes en 3er o 5to semestre (cursos más difíciles, mayor necesidad de info) y estudiantes en 10mo semestre (proyecto final de carrera).

**Value proposition:**

> Coaching académico personalizado de estudiantes y bachelors que ya cursaron la misma materia y —en el mejor caso— con el mismo profesor. Automatizado, respaldado por reseñas, de un UP a otro.
>
> **High-level concept:** *Airbnb for university knowledge*, donde los estudiantes monetizan lo que saben y los estudiantes con dificultades finalmente consiguen ayuda asequible.

### 7.2 Revenue model

#### Ingresos por servicios profesionales
Comisión del **15 %** sobre sesiones de tutoría reservadas vía plataforma.

| Concepto | Monto |
|---|---|
| Precio sesión de tutoría | S/40 |
| Comisión UPLearn (15 %) | S/6 |
| Ingreso del tutor | S/34 |

#### Ingresos por publicidad
Espacio publicitario para negocios estudiantiles y locales conectados a la comunidad. Integrado de forma **no intrusiva** para mantener UX positiva.

### 7.3 KPIs del producto

| Indicador | Mide |
|---|---|
| Estudiantes registrados | Adopción por ciclo. |
| Usuarios activos | Engagement regular con la plataforma. |
| Matches tutor–estudiante exitosos | Efectividad del matching peer-to-peer. |
| % estudiantes que encontraron info útil | Relevancia de recursos. |
| Oportunidades accesibles antes de deadlines | Efectividad para evitar perder deadlines. |
| Satisfacción (NPS) | UX y valor percibido. |
| Retención | Engagement de largo plazo. |

### 7.4 Impacto social esperado

| Dimensión | Impacto |
|---|---|
| Acceso a oportunidades | Becas, internships, intercambios, workshops. |
| Reducción de oportunidades perdidas | Información centralizada + recordatorios. |
| Mejor toma de decisiones académicas | Info confiable + reseñas de pares. |
| Mayor acceso a apoyo académico | Conexión con pares, tutores y recursos. |
| Comunidad estudiantil más fuerte | Compartir conocimiento entre ciclos. |
| Estrés ↓ | Estudiantes más confiados y preparados. |
| Éxito académico | Mejor desempeño + desarrollo integral. |

## 8. Capturas del MVP

> El MVP fue prototipado en Google AI Studio. *(Capturas pendientes — las subo en la próxima iteración de este case study.)*

<!--
Una vez que tengas las imágenes en /assets/img/uplearn-{login,dashboard,materials,reviews,tutoring,profile}.png, descomenta este bloque:

<figure class="figure-small">
  <img src="{{ '/assets/img/uplearn-login.png' | relative_url }}" alt="Login con correo institucional UP">
  <figcaption>Login restringido a <code>@up.edu.pe</code>. Donde nace la confianza.</figcaption>
</figure>

<figure class="figure-small">
  <img src="{{ '/assets/img/uplearn-dashboard.png' | relative_url }}" alt="Dashboard principal">
  <figcaption>Dashboard: estadísticas, recursos recientes, tutorías destacadas, negocios patrocinadores y accesos rápidos.</figcaption>
</figure>

<figure class="figure-small">
  <img src="{{ '/assets/img/uplearn-materials.png' | relative_url }}" alt="Materiales académicos">
  <figcaption>Materiales organizados por curso, con búsqueda y filtros.</figcaption>
</figure>

<figure class="figure-small">
  <img src="{{ '/assets/img/uplearn-reviews.png' | relative_url }}" alt="Reviews e insights">
  <figcaption>Reseñas de cursos y profesores para reducir la asimetría de información.</figcaption>
</figure>

<figure class="figure-small">
  <img src="{{ '/assets/img/uplearn-tutoring.png' | relative_url }}" alt="Tutoring peer-to-peer">
  <figcaption>Perfiles de tutor con rating, tarifa y disponibilidad — el motor de monetización.</figcaption>
</figure>

<figure class="figure-small">
  <img src="{{ '/assets/img/uplearn-profile.png' | relative_url }}" alt="Perfil de usuario">
  <figcaption>Perfil del estudiante con su actividad, materiales y sesiones agendadas.</figcaption>
</figure>
-->

## 9. Lo que aprendí haciendo este case study

1. **No todos los problemas son de tecnología — algunos son de distribución.** El material académico ya existe; el problema es que está secuestrado en círculos privados.
2. **El empathy map + sesgos cognitivos (availability bias, cognitive load) hacen un case study mucho más robusto** que solo interviews. Los sesgos son un diagnóstico de producto, no un adorno académico.
3. **Distinguir entre "producto social" y "negocio rentable" no es opcional.** Si el revenue model no cierra, el impacto se diluye. Comisión por tutoría + publicidad = estructura sostenible sin donantes.
4. **El MVP debe validar la hipótesis más arriesgada, no la más visible.** Lo arriesgado no era "¿la gente quiere una plataforma?" sino "¿estarían dispuestos a pagar por tutorías peer-to-peer?" — ahí debía enfocar la validación.
5. **El rol del PM en un proyecto sin dev es definir qué NO construir.** Recortamos funcionalidad de marketplace e-commerce a canal publicitario para reducir complejidad operativa y no atascarnos en logística de cobro/envío.

## 10. Conclusión

UPLearn demuestra el potencial de una **plataforma digital centralizada** para resolver el acceso fragmentado de los estudiantes a información académica, oportunidades y servicios de apoyo. Al integrar asesoría académica, tutorías, recursos universitarios y oportunidades en un solo espacio, **complementa el apoyo que ya brindan CEUP, consejos de facultad y asociaciones estudiantiles** y refuerza la colaboración, el engagement y el peer support dentro de la Universidad del Pacífico.

---

*Trabajo universitario realizado en la Universidad del Pacífico. Esta página es una reformatación orientada a case study PM del informe original del equipo.*