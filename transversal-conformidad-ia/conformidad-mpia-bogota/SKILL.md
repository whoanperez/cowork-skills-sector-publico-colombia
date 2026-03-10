---
name: conformidad-mpia-bogota
description: >
  Genera el paquete de conformidad MPIA-Bogotá para proyectos de IA en entidades
  distritales, conforme al Acuerdo 003 de 2025 de la Comisión Distrital de
  Transformación Digital. Calcula el Índice Compuesto de Madurez (ICM = 0,40×IGD
  + 0,60×PDP), clasifica la ruta de madurez (Exploratoria, Consolidación, Avanzada),
  genera el dictamen de conformidad por fase y produce el checklist de cumplimiento
  del lineamiento. Output: .docx con ficha técnica, diagnóstico IGD, cálculo PDP,
  dictamen ICM, clasificación de riesgos y plan de acción de cumplimiento.

  Usar SIEMPRE que alguien pida: conformidad MPIA, sello MPIA, diagnóstico de
  madurez IA, índice compuesto de madurez, cálculo ICM, evaluación MPIA, ruta de
  madurez IA, lineamiento distrital IA, Acuerdo 003, cumplimiento IA Bogotá,
  "necesito el sello MPIA", "cómo cumplo con el lineamiento de IA", "diagnóstico
  de mi proyecto de IA", "clasificar mi proyecto de IA", o cualquier variación
  que implique evaluar o documentar el cumplimiento de un proyecto de IA con el
  Acuerdo 003 de 2025 CDTD.
---

# Skill: Conformidad MPIA-Bogotá — Acuerdo 003/2025 CDTD

> Esta skill genera el paquete de conformidad MPIA-Bogotá para proyectos de
> inteligencia artificial en entidades del Distrito Capital. Evalúa el cumplimiento
> del Acuerdo 003 de 2025 de la Comisión Distrital de Transformación Digital y
> produce un dictamen con la ruta de madurez asignada.
>
> Leer `references/normativa_acuerdo003_2025.md` para el detalle normativo completo.

---

## Paso 0 — Recolección de información (en una sola interacción)

### Bloque A: Identificación del Proyecto de IA

1. **Nombre de la entidad distrital:** (ej: "Secretaría de Educación del Distrito",
   "UAECOB", "IDRD")

2. **Nombre del proyecto o sistema de IA:** (ej: "Asistente documental con IA
   generativa", "Modelo predictivo de deserción escolar")

3. **Categoría del sistema** (seleccione una o más):
   - [ ] a) Automatización avanzada / RPA con impacto administrativo
   - [ ] b) Analítica predictiva y modelos de aprendizaje automático
   - [ ] c) Sistemas de recomendación o priorización algorítmica
   - [ ] d) Chatbots, asistentes virtuales y sistemas de interacción automatizada
   - [ ] e) Visión por computador y análisis automatizado de imágenes/video
   - [ ] f) OCR con extracción automatizada
   - [ ] g) Inteligencia Artificial Generativa
   - [ ] h) Tecnologías emergentes o híbridas

4. **Descripción del proyecto en 3-5 líneas:**
   - ¿Qué problema público resuelve?
   - ¿Cuál es el valor público esperado?
   - ¿Cuál es la población beneficiaria?

5. **Estado actual:**
   - [ ] En fase de idea
   - [ ] En prototipo/piloto
   - [ ] En ejecución con plan aprobado
   - [ ] En operación institucional
   - [ ] En producción con interacción ciudadana

6. **¿El proyecto afecta infraestructura crítica o servicios esenciales?**
   (Decreto Nacional 88/2022, Decreto Distrital 472/2024)
   - [ ] Sí → Se activa Ruta Especial ICC/SE
   - [ ] No

7. **¿El proyecto trata datos personales?**
   - [ ] No trata datos personales
   - [ ] Trata datos personales no sensibles
   - [ ] Trata datos personales sensibles o de menores

8. **¿Tiene plantilla institucional .docx?** (Si sí, cargarla)

### Bloque B: Índice de Gobierno Digital (IGD)

9. **¿La entidad está incluida en la medición del IGD del MinTIC/FURAG?**
   - [ ] Sí → Proporcionar los valores de los 11 subíndices (escala 0-100)
   - [ ] No → Se aplicará la autoevaluación documentada

10. **Si la entidad SÍ está en el IGD, proporcionar los valores de los 11 subíndices:**

    | N° | Subíndice | Valor (0-100) |
    |---|---|---|
    | 1 | TIC para el Estado | |
    | 2 | TIC para la Sociedad | |
    | 3 | Gobernanza de TI | |
    | 4 | Seguridad y Privacidad de la Información | |
    | 5 | Servicios Ciudadanos Digitales | |
    | 6 | Gobierno Abierto | |
    | 7 | Decisiones basadas en datos | |
    | 8 | Fortalecimiento de capacidades | |
    | 9 | Arquitectura TI | |
    | 10 | Interoperabilidad | |
    | 11 | Uso y apropiación | |

    **Fuente de los datos:** (FURAG, portal MinTIC, autoevaluación)
    **Fecha de corte:** (ej: diciembre 2024)

11. **Si la entidad NO está en el IGD**, se realizará una autoevaluación documentada
    (0-100) con base en evidencia verificable para cada subíndice. Se utilizará
    el formato "Autoevaluacion_IGD_IA_NoObligados_PDP_V1a".

### Bloque C: Puntaje por Determinantes del Proyecto (PDP)

12. **Para cada factor, asignar un valor (0, 5 o 10) con base en la evidencia disponible:**

    | Factor | 0 = No cumple | 5 = Parcial | 10 = Completo | Valor | Evidencia |
    |---|---|---|---|---|---|
    | 1. Inclusión en PETI | No figura en PETI ni instrumentos de planeación | Figura sin metas/cronograma | Priorizado con metas, responsables y cronograma | | |
    | 2. Recursos económicos asignados | Sin recursos ni fuente de financiación | Financiación parcial/temporal (CAPEX u OPEX solo piloto) | Recursos para todo el ciclo de vida (desarrollo, mantenimiento, evaluación) | | |
    | 3. Alcance institucional | Una sola dependencia | Varias dependencias de la entidad | Transversal o vincula varias entidades del sector/Distrito | | |
    | 4. Modelo de sostenibilidad | No existe modelo ni presupuesto | Modelo/presupuesto preliminar o <1 año, sin cobertura total | Modelo formal >1 año que cubre operación, monitoreo, actualización, formación | | |
    | 5. Estado de ejecución y plan de cumplimiento | No ha iniciado o sin plan | En ejecución con plan aprobado y plazo ≤60 días | En ejecución activa, cumple lineamientos IA responsable, evidencia trazable | | |
    | 6. Infraestructura crítica / servicio esencial (ICC/SE) | No afecta servicios esenciales ni infraestructura crítica | *(No aplica — escala binaria)* | Afecta directamente servicios esenciales o infraestructura crítica → Ruta ICC/SE | | |
    | 7. Manuales de uso y operación | No existen manuales ni guías técnicas | Borradores en revisión sin cobertura completa de roles/flujos/soporte | Aprobados, actualizados, divulgados, con mecanismos de actualización | | |
    | 8. Tratamiento de datos personales | Sin base jurídica ni política de tratamiento, sin controles | EIA/DPIA preliminar, medidas de minimización sin finalizar | EIA/DPIA completa, medidas de minimización, cláusulas contractuales, avisos de privacidad vigentes | | |

### Bloque D: Contexto adicional

13. **¿La entidad cuenta con los siguientes roles designados para el proyecto?**
    - [ ] Punto focal jurídico
    - [ ] Punto focal TIC/Infraestructura
    - [ ] Punto focal Datos/Gobernanza
    - [ ] Punto focal Seguridad de la Información
    - [ ] Responsable de dependencia misional
    - [ ] Supervisor/interventor (si hay proveedor externo)

14. **¿Existe expediente digital del proyecto?** (repositorio de evidencias conforme
    a normas de gestión documental)
    - [ ] Sí, estructurado con control de versiones
    - [ ] Sí, pero informal o incompleto
    - [ ] No existe

15. **¿El proyecto ya tiene conexión con el canal distrital de comunicaciones?**
    (Bogotá Te Escucha o equivalente)
    - [ ] Sí, operativo y documentado
    - [ ] En proceso
    - [ ] No

---

## Paso 1 — Cálculos y clasificación

### 1.1 Cálculo del IGD

```
IGD = Promedio de los 11 subíndices

Si la entidad NO está en la medición, aplicar autoevaluación documentada.
```

**Condición de criticidad (obligatoria):**
- Si Gobernanza, Seguridad y Privacidad de la Información, o Decisiones basadas
  en datos < 40 → La ruta NO puede superar Consolidación
- Si cualquiera de los tres < 30 → Exploratoria obligatoria

### 1.2 Cálculo del PDP

```
PDP = Σ ((Valor_i / 10) × Peso_i)

Donde:
- Factor 6 (ICC/SE): escala binaria (0 o 10), peso 20%
- Factores 1-5, 7-8: escala 0/5/10, pesos según tabla
```

### 1.3 Cálculo del ICM

```
ICM = 0,40 × IGD + 0,60 × PDP
```

### 1.4 Asignación de ruta de madurez

| Rango ICM | Ruta |
|---|---|
| 0 – 39 | Exploratoria |
| 40 – 69 | Consolidación |
| 70 – 100 | Avanzada |

**Reglas especiales:**
1. Si el proyecto ya está en ejecución sin plan aprobado → no puede superar Consolidación
2. Si es ICC/SE → Ruta Especial con controles de nivel Avanzado obligatorios desde Fase 2
3. Verificar condición de criticidad del IGD (subíndices Gobernanza, Seguridad, Datos)

### 1.5 Clasificación de riesgo del sistema de IA

Con base en la categoría del sistema, el estado, el tratamiento de datos y la
interacción con ciudadanía, clasificar en:
- **Bajo:** Apoyo operativo, sin decisiones, sin datos sensibles, sin interacción ciudadana
- **Medio:** Apoya decisiones internas, datos no sensibles, exposición moderada
- **Alto:** Influye en decisiones administrativas, interactúa con ciudadanía, datos sensibles
- **Crítico:** Incide en derechos fundamentales, infraestructura crítica, alto impacto social

---

## Paso 2 — Generación del documento de conformidad

### Estructura del documento .docx

El documento se titula: **"Dictamen de Conformidad MPIA-Bogotá — [Nombre del Proyecto]"**

**Secciones obligatorias:**

#### Sección 1: Ficha técnica del proyecto
- Nombre del proyecto, entidad, dependencia responsable
- Categoría del sistema de IA (a-h del Acuerdo)
- Descripción: problema público, valor público esperado, población beneficiaria
- Estado actual
- Clasificación ICC/SE

#### Sección 2: Diagnóstico IGD
- Tabla con los 11 subíndices, valores y semáforo (Rojo/Ámbar/Verde)
- Fuente y fecha de corte
- Resultado IGD (promedio)
- Verificación de condición de criticidad
- Observaciones y brechas identificadas

#### Sección 3: Puntaje por Determinantes del Proyecto (PDP)
- Tabla con los 8 factores, valores asignados, pesos, valor ponderado y evidencia
- Resultado PDP total
- Verificación de reglas especiales (ICC/SE, ejecución sin plan)
- Observaciones por factor

#### Sección 4: Índice Compuesto de Madurez (ICM) y Ruta Asignada
- Cálculo: ICM = 0,40 × IGD + 0,60 × PDP
- Ruta de madurez asignada con justificación
- Aplicación de condiciones de criticidad y reglas especiales
- Si aplica Ruta Especial ICC/SE, indicarlo expresamente

#### Sección 5: Clasificación de riesgo del sistema de IA
- Nivel de riesgo asignado (Bajo / Medio / Alto / Crítico)
- Justificación con base en criterios de impacto y probabilidad del Acuerdo
- Controles mínimos obligatorios según nivel de riesgo

#### Sección 6: Checklist de cumplimiento — Fase 1 (Preparación y Planeación)
Evaluación de cumplimiento de los requisitos de la Fase 1:

- [ ] Ficha técnica del proyecto elaborada (objetivo, alcance, valor público, población)
- [ ] Diagnóstico IGD obtenido o autoevaluado con evidencia
- [ ] PDP calculado con valores, pesos y evidencias documentadas
- [ ] ICM calculado y ruta de madurez asignada
- [ ] Condición de criticidad verificada (subíndices Gobernanza, Seguridad, Datos)
- [ ] Clasificación ICC/SE verificada
- [ ] Plan de trabajo con responsables, agenda y repositorio de evidencias
- [ ] Expediente digital del proyecto creado con control de versiones
- [ ] Actores institucionales identificados (Jurídica, TIC, Datos, Seguridad, Misional)

#### Sección 7: Checklist de cumplimiento — Requisitos Generales Transversales (Fase 2)

**Gobernanza institucional:**
- [ ] Matriz de alineación institucional elaborada (proyecto vs. IGD + políticas distritales)
- [ ] Archivada en expediente digital con fecha de corte

**Roles y responsabilidades:**
- [ ] Listado oficial de roles ("quién hace qué") documentado
- [ ] Incluye puntos focales de: Jurídica, TIC, Datos, Seguridad, Misional
- [ ] Si hay proveedor externo: supervisor/interventor designado

**Conexión canal distrital:**
- [ ] Proyecto integrado a Bogotá Te Escucha o canal equivalente
- [ ] Punto de conexión y responsable de escalamiento registrados
- [ ] Prueba de recepción (ticket o caso de prueba) documentada

**Línea base PDP:**
- [ ] Matriz de línea base PDP registrada con fecha de corte
- [ ] Mecanismo de actualización definido

**Clasificación de riesgos:**
- [ ] Modelo de clasificación de riesgos adoptado (niveles: bajo, medio, alto, crítico)
- [ ] Criterios de impacto y probabilidad documentados
- [ ] Controles mínimos definidos según nivel de riesgo
- [ ] Resultados archivados en expediente digital

**Uso responsable de IA Generativa (si categoría g):**
- [ ] Usos permitidos y no permitidos establecidos
- [ ] Supervisión y validación humana garantizada antes de cualquier efecto administrativo
- [ ] Salvaguardas contra sesgos, errores y desinformación implementadas
- [ ] Evidencia conservada en expediente digital

**Etiquetado de contenido IA:**
- [ ] Estándares de etiquetado adoptados para contenido asistido por IA
- [ ] Identificación clara, visible y verificable del origen algorítmico
- [ ] Procedimientos de etiquetado y validación documentados

**Supervisión humana:**
- [ ] Capacidad real de revisión, validación y reversión de resultados
- [ ] Registro de intervenciones humanas y sus decisiones
- [ ] Personal responsable designado y capacitado

**Transparencia algorítmica:**
- [ ] Contenido mínimo de divulgación preparado (9 campos obligatorios)
- [ ] Publicación en sitio web institucional (menú de transparencia)
- [ ] Canal de objeciones y solicitudes de revisión habilitado

**Protección de datos personales:**
- [ ] Política Distrital de Protección de Datos aplicada
- [ ] Documentado si el sistema trata datos personales (base jurídica, finalidad, medidas)
- [ ] DPIA completada (si aplica)
- [ ] Cláusulas contractuales con terceros (si aplica)

**Seguridad digital:**
- [ ] Estrategia Distrital de Ciberseguridad aplicada
- [ ] Punto focal de seguridad digital designado
- [ ] Controles de nivel Avanzado aplicados (si ICC/SE)

#### Sección 8: Checklist específico por ruta de madurez

*Se genera solo la sección correspondiente a la ruta asignada (Exploratoria, Consolidación o Avanzada), con los controles específicos de esa ruta.*

#### Sección 9: Plan de acción de cumplimiento
Para cada ítem del checklist que NO se cumpla:

| N° | Requisito incumplido | Referencia en el Acuerdo | Acción requerida | Responsable sugerido | Plazo sugerido | Prioridad |
|---|---|---|---|---|---|---|
| 1 | ... | Art./Numeral | ... | Área | ... | Alta/Media/Baja |

#### Sección 10: Dictamen final

**Formato del dictamen:**

```
DICTAMEN DE CONFORMIDAD MPIA-BOGOTÁ

Proyecto: [Nombre]
Entidad: [Nombre]
Fecha del dictamen: [DD/MM/AAAA]

Resultado IGD: [XX.X] / 100
Resultado PDP: [XX.X] / 100
Índice Compuesto de Madurez (ICM): [XX.X] / 100

Ruta de madurez asignada: [Exploratoria / Consolidación / Avanzada]
Ruta Especial ICC/SE: [Sí / No]
Clasificación de riesgo: [Bajo / Medio / Alto / Crítico]

Fase 1 (Preparación): [X/9 requisitos cumplidos] — [Cumple / No cumple]
Fase 2 (Requisitos Generales): [X/Y requisitos cumplidos] — [Cumple / Cumple parcialmente / No cumple]
Fase 2 (Requisitos por Ruta): [X/Y requisitos cumplidos] — [Cumple / Cumple parcialmente / No cumple]

DICTAMEN GENERAL: [CONFORME / CONFORME CON OBSERVACIONES / NO CONFORME]

Observaciones:
[Texto libre con los hallazgos principales y recomendaciones]

Este dictamen tiene carácter orientador y de autoevaluación. No constituye
certificación oficial por parte de la Consejería Distrital de TIC.
La entidad conserva la responsabilidad integral sobre la veracidad de la
información y la trazabilidad de las evidencias.
```

---

## Paso 3 — Formato y presentación del documento

### Si el usuario proporcionó plantilla institucional .docx:
- Extraer estilos, encabezado, pie de página, fuentes y colores institucionales
- Aplicar esos estilos al documento de dictamen
- Mantener el escudo institucional si está presente

### Si NO hay plantilla:
```
Formato base:
- Tamaño página: Carta (21.59 × 27.94 cm)
- Márgenes: Superior 3cm, Inferior 2.5cm, Izquierdo 3cm, Derecho 2.5cm
- Fuente títulos: Arial 14pt negrita
- Fuente subtítulos: Arial 12pt negrita
- Fuente cuerpo: Arial 11pt
- Fuente tablas: Arial 10pt
- Espaciado: 1.15
- Colores de semáforo en tablas:
  - Verde (70-100): RGB(0, 176, 80)
  - Ámbar (40-69): RGB(255, 192, 0)
  - Rojo (0-39): RGB(255, 0, 0)
```

Nombre del archivo:
`Dictamen_MPIA_[NombreEntidad]_[NombreProyecto]_[AAAAMMDD].docx`

---

## Paso 4 — Metadatos SGDEA

```
Tipo documental: Dictamen técnico
Serie documental: Proyectos de Inteligencia Artificial
Subserie: Conformidad MPIA-Bogotá
Fecha: [DD/MM/AAAA]
Folios: [número de páginas]
Soporte: Electrónico
Elaboró: [Nombre y cargo del responsable]
Dependencia: [Oficina TIC / Planeación / según estructura]
Marco normativo: Acuerdo 003 de 2025 CDTD
```

---

## Marco normativo embebido

Ver `references/normativa_acuerdo003_2025.md` para el texto completo de referencia.

**Normas principales:**
- **Acuerdo 003 de 2025 CDTD** — Lineamientos técnicos y éticos en IA para el Distrito Capital
- **Acuerdo Distrital 1017/2025** — Ordena expedición de lineamientos de IA responsable
- **Decreto Distrital 025/2021** — Comisión Distrital de Transformación Digital
- **Acuerdo 927/2024 Art. 228** — PDD "Bogotá Camina Segura" — transformación digital
- **Decreto Nacional 1078/2015** — Decreto Único del Sector TIC
- **Decreto Nacional 88/2022** — Infraestructura Crítica Cibernética
- **Directiva Conjunta 007/2025** — Transparencia algorítmica (PGN + Defensoría)
- **Ley 1581/2012** — Protección de Datos Personales
- **Ley 1712/2014** — Transparencia y acceso a la información pública

---

## Notas de uso

- **Esta skill genera un dictamen de autoevaluación.** No es una certificación oficial
  de la Consejería Distrital de TIC.
- **La responsabilidad sobre la veracidad de la información es de la entidad.**
  Las evidencias son sujetas a verificación posterior por órganos de control.
- **La ruta de madurez no requiere aprobación previa** para avanzar entre fases,
  pero sí requiere cumplir integralmente los requisitos de cada fase.
- **Para proyectos con proveedor externo**, incluir los datos del contratista
  en la sección de roles y responsabilidades.
- **Si la entidad no tiene todos los datos**, indicar "Pendiente" en los campos
  faltantes y generar un plan de acción para obtenerlos.
- **Esta skill se complementa con las demás skills del portafolio** — los documentos
  generados por otras skills (oficios, informes, planes de acción, matrices de riesgo)
  incluyen automáticamente el sello de conformidad MPIA.

---

## Conexión con otras skills del portafolio

| Skill | Relación con conformidad MPIA |
|---|---|
| oficio-memorando-entidad | El sello MPIA se incluye en el pie del documento generado |
| respuesta-pqrsdf-entidad | Clasificación de riesgo "Medio" por interacción con ciudadanía |
| acta-reunion-entidad | Trazabilidad de uso de IA documentada |
| informe-gestion-entidad | Etiquetado de contenido IA incluido |
| plan-accion-entidad | Alineación con IGD y políticas distritales |
| ficha-indicador-entidad | KPIs de monitoreo del sistema de IA |
| matriz-riesgos-entidad | Clasificación de riesgos conforme al modelo MPIA |
| mga-proyecto-inversion | Formulación de proyecto de IA con estructura MGA |
