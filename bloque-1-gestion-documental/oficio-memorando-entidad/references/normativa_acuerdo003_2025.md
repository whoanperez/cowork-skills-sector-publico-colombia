# Normativa de Referencia — Acuerdo 003 de 2025 CDTD
# Lineamientos Técnicos y Éticos en IA para el Distrito Capital de Bogotá

## 1. Datos del Acuerdo

- **Nombre:** Acuerdo No. 003 de 26 de diciembre de 2025
- **Expedido por:** Comisión Distrital de Transformación Digital — CDTD
- **Objeto:** Adoptar lineamientos y estándares para la preparación, desarrollo, implementación, supervisión y mejora continua de los sistemas de IA en entidades y organismos del Distrito Capital
- **Alcance:** Obligatorio para entidades del sector central, descentralizado y localidades del Distrito Capital
- **Vigencia:** A partir del 27 de diciembre de 2025
- **Registro Distrital:** No. 8488, Año 60

---

## 2. Marco Normativo de Soporte

| Norma | Contenido relevante |
|---|---|
| Constitución Política Art. 113, 209 | Colaboración armónica, coordinación administrativa |
| Decreto Ley 1421/1993 Art. 38 | Facultades del Alcalde Mayor |
| Decreto Distrital 025/2021 | Crea la Comisión Distrital de Transformación Digital |
| Decreto Distrital 140/2021 Art. 11 | Funciones de la Consejería Distrital de TIC |
| Decreto Distrital 575/2023 | Marco de transformación digital distrital |
| Acuerdo 927/2024 Art. 228 | PDD "Bogotá Camina Segura" — transformación digital y ciudad inteligente |
| Acuerdo Distrital 1017/2025 | Ordena expedición de lineamientos de IA responsable |
| Decreto Nacional 1078/2015 | Decreto Único del Sector TIC — Política de Gobierno Digital |
| Decreto Nacional 767/2022 | Política de Gobierno Digital actualizada |
| Resolución MinTIC 460/2022 | Marco de Interoperabilidad |
| Decreto Nacional 88/2022 | Infraestructura Crítica Cibernética |
| Directiva Conjunta 007/2025 PGN-Defensoría | Transparencia algorítmica |
| Ley 1581/2012 | Protección de Datos Personales |
| Ley 1712/2014 | Transparencia y acceso a la información pública |
| Ley 1755/2015 | Derecho fundamental de petición |

---

## 3. Modelo MPIA-Bogotá (Modelo de Preparación e Implementación)

### 3.1 Estructura: Ciclo PHVA

| Fase PHVA | Fase del Modelo | Actividades principales |
|---|---|---|
| Planear | Fase 1 — Preparación y Planeación | Diagnóstico IGD, cálculo PDP, ICM, clasificación de ruta, plan de trabajo |
| Hacer | Fase 2 — Desarrollo, Validación y Despliegue | Requisitos generales + específicos por ruta, controles técnicos/éticos |
| Verificar | Fase 3 — Implementación y Seguimiento | Monitoreo, auditorías, EIA/DPIA, indicadores KPI/OKR |
| Actuar | (dentro de Fase 3) | Reentrenamiento, gestión de terceros, cierre de ciclo, lecciones aprendidas |

### 3.2 Índice Compuesto de Madurez (ICM)

**Fórmula:** ICM = 0,40 × IGD + 0,60 × PDP

**Rangos de madurez:**

| Rango ICM | Ruta de madurez |
|---|---|
| 0 – 39 | Exploratoria |
| 40 – 69 | Consolidación |
| 70 – 100 | Avanzada |

### 3.3 Índice de Gobierno Digital (IGD)

- 11 elementos/subíndices del MinTIC (escala 0-100)
- Fuente: https://gobiernodigital.mintic.gov.co/portal/Mediciones/ o FURAG
- Semáforo por subíndice: Rojo (0-39), Ámbar (40-69), Verde (70-100)
- **Condición de criticidad:** Si Gobernanza, Seguridad y Privacidad de la Información, o Decisiones basadas en datos obtiene <40 → no puede superar Consolidación; <30 → Exploratoria obligatoria

### 3.4 Puntaje por Determinantes del Proyecto (PDP)

**8 factores ponderados:**

| Factor | Peso (%) | Valores posibles |
|---|---|---|
| 1. Inclusión en PETI | 10 | 0 / 5 / 10 |
| 2. Recursos económicos asignados | 15 | 0 / 5 / 10 |
| 3. Alcance institucional | 10 | 0 / 5 / 10 |
| 4. Modelo de sostenibilidad | 15 | 0 / 5 / 10 |
| 5. Estado de ejecución y plan de cumplimiento | 10 | 0 / 5 / 10 |
| 6. Infraestructura crítica / servicio esencial (ICC/SE) | 20 | 0 / 10 (binario) |
| 7. Manuales de uso y operación | 10 | 0 / 5 / 10 |
| 8. Tratamiento de datos personales | 10 | 0 / 5 / 10 |
| **TOTAL** | **100** | |

**Fórmula:** PDP = Σ ((Valor / 10) × Peso)

### 3.5 Ruta Especial ICC/SE

Si el proyecto afecta infraestructura crítica o servicios esenciales (Decreto Nacional 88/2022, Decreto Distrital 472/2024):
- Aplican controles de nivel Avanzado obligatorios desde Fase 2
- Independientemente del ICM calculado

---

## 4. Categorías de Sistemas de IA Cubiertas

| Categoría | Descripción | Obligaciones especiales |
|---|---|---|
| a) RPA con impacto administrativo | Automatizaciones que modifican registros o procesan información sensible | Controles de integridad |
| b) Analítica predictiva | Modelos de aprendizaje automático | Validación periódica, gestión de sesgos |
| c) Recomendación/priorización | Sistemas que influyen en decisiones | Explicabilidad, responsabilidad humana |
| d) Chatbots/asistentes virtuales | Interacción con ciudadanía | Transparencia, supervisión humana, protección de datos |
| e) Visión por computador | Análisis de imágenes/video | Controles de identificación, supervisión significativa |
| f) OCR con extracción automatizada | Alimenta decisiones o procesos operativos | Validación de exactitud |
| **g) IA Generativa** | **Produce texto, imágenes, video o código para comunicaciones oficiales** | **Supervisión humana, controles de calidad, salvaguardas éticas, trazabilidad** |
| h) Tecnologías emergentes/híbridas | Cualquier otra que produzca resultados relevantes | Según naturaleza |

---

## 5. Requisitos Generales Transversales (Fase 2 — todas las rutas)

### 5.1 Gobernanza institucional (7.5.1.1)
- Matriz de alineación institucional (IGD + políticas distritales)
- Herramienta: "Matriz_Alineacion_Institucional_IGD_IA_V1"
- Resultado: Matriz archivada en expediente digital

### 5.2 Roles y responsabilidades (7.5.2)
- Puntos focales: Jurídica, TIC/Infraestructura, Datos/Gobernanza, Seguridad, Dependencia misional
- Herramienta: "Matriz_Roles_Responsabilidades_IA_V1"
- Resultado: Listado oficial de roles ("quién hace qué")

### 5.3 Transparencia algorítmica (7.5.2.3)
**Contenido mínimo de divulgación (publicar en sitio web):**
1. Nombre del sistema y versión
2. Propósito y uso previsto
3. Función institucional o proceso
4. Estado (en desarrollo, implementado, suspendido, descontinuado)
5. Si trata datos personales
6. Tipología general de datos utilizados
7. Entidad o proveedor responsable
8. Canales de contacto para objeciones (plazos de Ley 1755/2015)
9. Fecha de última actualización

**Actualización:** Anual o ante cambios sustanciales

### 5.4 Protección de datos personales (7.5.2.5)
- Cumplimiento de Política Distrital de Protección de Datos
- Ley 1581/2012, Decreto 1377/2013
- DPIA cuando aplique (Art. 2.2.17.5.2 Decreto 1078/2015)
- Cláusulas contractuales con terceros

### 5.5 Seguridad digital (7.5.2.6)
- Estrategia Distrital de Ciberseguridad
- Punto focal de seguridad digital por proyecto
- ICC/SE: controles de nivel Avanzado obligatorios

---

## 6. Clasificación de Riesgos para Sistemas de IA

| Nivel | Descripción | Criterios de Impacto | Criterios de Probabilidad |
|---|---|---|---|
| 1. Bajo | Apoyo operativo, sin incidencia en decisiones, sin datos sensibles | No afecta decisiones, no procesa datos sensibles, no interactúa con ciudadanía | Baja probabilidad de error, baja complejidad |
| 2. Medio | Apoya decisiones internas no discrecionales | Puede influir en clasificaciones, procesa datos no sensibles | Probabilidad media de error/sesgo, exposición moderada |
| 3. Alto | Influye en decisiones administrativas, interactúa con ciudadanía | Procesa datos sensibles, interactúa con grupos vulnerables, impacto significativo | Probabilidad relevante de error, complejidad técnica alta |
| 4. Crítico | Incide en decisiones de alto impacto social | Afecta derechos fundamentales, infraestructura crítica | Incluso baja probabilidad implica consecuencias severas |

---

## 7. Requisitos por Ruta de Madurez

### 7.1 Nivel Exploratorio (ICM 0-39)
**Alcance:** Proyectos en fase de idea, prototipo o piloto
**Controles mínimos:**
- Explicar problema público y beneficio esperado
- Enumerar riesgos técnicos, jurídicos y éticos
- Usar datos anonimizados, sintéticos o de dominio público
- Registrar modelo/técnica utilizada y fuente de datos
- Documentar responsables y fecha de inicio
**Evidencias:** Documento con propósito y valor público, listado de riesgos, descripción técnica, origen de datos, registro de comunicación al canal distrital

### 7.2 Nivel Consolidación (ICM 40-69)
**Alcance:** Proyectos con resultados o pilotos validados
**Controles adicionales:**
- Plan de trabajo con cronograma e indicadores de desempeño
- Revisión de riesgos con impacto × probabilidad
- Base jurídica válida y DPIA cuando corresponda
- Pruebas de precisión, estabilidad y confiabilidad documentadas
- Explicabilidad en lenguaje comprensible
- Concepto jurídico-técnico de cumplimiento
**Evidencias:** Plan de ejecución, matriz de riesgos, registro de pruebas, documentación de explicabilidad, concepto jurídico-técnico

### 7.3 Nivel Avanzado (ICM 70-100)
**Alcance:** Proyectos en operación institucional
**Controles adicionales:**
- Auditorías técnicas/algorítmicas anuales (internas o externas)
- Supervisión humana con documentación de revisiones
- Procedimiento de reentrenamiento/ajuste de modelo
- Plan de continuidad y pruebas de contingencia
- Monitoreo continuo de desempeño (KPIs)
- Análisis de impacto actualizado (DPIA + EIA)
- Publicación de información de transparencia reforzada
**Evidencias:** Informe/acta de auditoría, registro de supervisión humana, procedimiento de reentrenamiento, plan de continuidad, monitoreo continuo, análisis de impacto

---

## 8. Uso Cotidiano de IA en el Distrito Capital (Sección 10)

### 8.1 Definición
Uso de modelos de lenguaje generativo, herramientas tipo GPT y tecnologías equivalentes para apoyar tareas rutinarias de servidores públicos. Naturaleza asistencial, de bajo impacto.

### 8.2 Actividades permitidas
- Generación y organización de ideas
- Redacción, corrección, estructuración o síntesis de textos institucionales
- Resúmenes, cálculos simples y análisis preliminares
- Preparación de insumos para documentos, informes o presentaciones
- Clasificación básica de información
- Búsqueda, explicación rápida de conceptos técnicos o normativos
- Organización de agenda, recordatorios o apoyo operativo documental

### 8.3 Condiciones obligatorias
1. La IA es SOLO herramienta de asistencia — **prohibido** sustituir análisis, interpretación, deliberación técnica, valoración probatoria, adopción de decisiones o formulación de políticas
2. Todo contenido generado debe ser **revisado, corregido y validado** por el funcionario
3. La **aprobación humana** es condición para incorporar en: comunicaciones institucionales, documentos internos/externos, análisis administrativos/jurídicos, informes o borradores para toma de decisiones
4. Cuando se use IA, debe dejarse **constancia de**: herramienta utilizada, tipo de apoyo recibido, alcance de la intervención humana
5. **Trazabilidad obligatoria** en: informes técnicos, documentos divulgados públicamente, comunicaciones oficiales, insumos para toma de decisiones
6. El servidor público es el **único responsable** por los contenidos producidos con apoyo de IA

### 8.4 Prohibiciones expresas
- Automatizar decisiones o acciones administrativas
- Generar actos administrativos o sus motivaciones
- Producir documentos jurídicos vinculantes
- Replicar información sin verificación
- Elaborar documentos que deban ajustarse a formatos oficiales específicos, SIN revisión humana
- Ingresar en herramientas no institucionales: datos personales/sensibles, información sujeta a reserva, documentos oficiales no publicados, información estratégica/contractual/financiera, archivos protegidos por propiedad intelectual, datos de sistemas críticos

### 8.5 Regla de oro
> "El juicio técnico, profesional y ético del funcionario prevalece SIEMPRE sobre cualquier contenido generado por IA."

---

## 9. Herramientas oficiales del MPIA-Bogotá

| Herramienta | Propósito |
|---|---|
| ICM_MPIA_Bogota_V1 | Cálculo del Índice Compuesto de Madurez |
| Autoevaluacion_IGD_IA_NoObligados_PDP_V1a | Autoevaluación IGD para entidades no obligadas |
| Matriz_Alineacion_Institucional_IGD_IA_V1 | Articulación proyecto vs. políticas distritales e IGD |
| Matriz_Roles_Responsabilidades_IA_V1 | Roles y responsabilidades en el ciclo PHVA |
| Matriz_Linea_Base_Factores_Determinantes_Proyecto_V1 | Línea base PDP con trazabilidad de cambios |

---

## 10. Aplicabilidad a Skills de IA Generativa para Documentos Oficiales

### 10.1 Clasificación del portafolio de skills

Las skills de generación de documentos oficiales para entidades distritales califican como:
- **Categoría:** (g) Sistemas de Inteligencia Artificial Generativa
- **Nivel de riesgo probable:** Bajo a Medio (asistencia documental sin toma de decisiones autónoma)
- **Sección aplicable principal:** 10 — Uso Cotidiano de la IA
- **Ruta de madurez probable:** Exploratoria (ICM < 40 para mayoría de entidades en adopción inicial)

### 10.2 Obligaciones que las skills deben facilitar

| Obligación del Acuerdo | Cómo la skill lo cumple |
|---|---|
| Etiquetado de contenido IA (7.5.2.2.4) | Pie de página: "Documento generado con asistencia de IA — requiere revisión y aprobación humana" |
| Supervisión humana (7.5.2.2.5, 10.3) | El output es BORRADOR, no documento final. Checklist de revisión incluido |
| Trazabilidad (10.4) | Metadatos de trazabilidad IA en cada documento generado |
| Clasificación de riesgo (7.5.2.2.1) | Nivel de riesgo indicado en checklist de conformidad |
| No sustituye juicio humano (10.1) | Advertencia explícita: "No sustituye el criterio profesional del servidor público" |
| Prohibición de datos sensibles (10.4) | Advertencia de no ingresar datos personales sensibles o reservados |
| Responsabilidad del servidor (10.6) | Cláusula de responsabilidad del firmante, no de la herramienta |
