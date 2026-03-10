---
name: informe-control-interno-entidad
description: >
  Genera Informes de Control Interno / Auditoría Interna para entidades del sector público
  colombiano, conforme a Ley 87/1993, Decreto 1499/2017 Dimensión 7, Decreto 648/2017.
  Soporta múltiples modalidades: evaluación independiente del SCI (semestral), informe
  pormenorizado cuatrimestral, seguimiento al PAAC, auditorías internas de procesos/proyectos.
  Estructura hallazgos con criterio-condición-causa-efecto-evidencia. Output en formato
  Word (.docx). ADVERTENCIA: IA estructura el informe; auditoría la realiza personal calificado.

  Usar SIEMPRE que alguien pida: control interno, auditoría interna, evaluación SCI,
  informe de hallazgos, evaluación de gestión institucional, seguimiento al PAAC,
  auditoría de proceso, Decreto 1499 Dimensión 7, "cómo estructuramos el informe de
  auditoría", "reporte de hallazgos", o cualquier variación que implique generar informe
  de control interno o auditoría interna institucional.
---

# Skill: Informe de Control Interno / Auditoría Interna

> Esta skill genera informes de control interno en Word (.docx), alineados con Ley 87/1993
> (Control Interno), Decreto 1499/2017 Dimensión 7 (Control Interno del MIPG) y Decreto
> 648/2017 (Roles de oficina de control). Soporta cuatro modalidades: a) Evaluación
> independiente del SCI (semestral para DAFP), b) Informe pormenorizado cuatrimestral
> (publicación web), c) Seguimiento al PAAC cuatrimestral, d) Auditoría interna de
> procesos/proyectos específicos. Leer `references/normativa_transparencia.md` para
> normativa, roles y estructura de hallazgos.
>
> **ADVERTENCIA CRÍTICA:** Esta skill estructura el informe y propone hallazgos basados en
> información suministrada. La auditoría EN SÍ (ejecución de procedimientos, validación de
> evidencia, juicio profesional) debe ser realizada por personal calificado de control
> interno/auditoría. La IA NO REALIZA AUDITORÍA.

---

## Paso 0 — Clasificación y recolección

### Preguntas obligatorias (en una sola interacción)

1. **Tipo de informe:**
   - a) Evaluación independiente del SCI (semestral, reporte a DAFP)
   - b) Informe pormenorizado de control interno (cuatrimestral, web pública)
   - c) Seguimiento al PAAC (cuatrimestral, web pública)
   - d) Auditoría interna de proceso específico (ad hoc)
   - Otro (especificar)

2. **Período cubierto:**
   - Fechas de inicio y fin
   - Períodos anteriores para comparación (si existen informes previos)

3. **Tipo de entidad:**
   - Entidad de orden nacional (ministerio, departamento administrativo)
   - Entidad territorial (gobernación, municipio, distrito)
   - Entidad descentralizada (instituto, empresa pública, fondo)
   - Otro (especificar)

4. **Para auditoría interna de proceso (si aplica):**
   - ¿Cuál es el proceso auditado? (descripción, responsables)
   - ¿Período cubierto?
   - ¿Alcance: actividades específicas o toda la cadena?
   - ¿Criterios de evaluación? (normas, políticas, leyes aplicables)
   - ¿Se han realizado auditorías anteriores a este proceso?

5. **Hallazgos identificados (si el auditor ya tiene):**
   - Hallazgo 1: Criterio | Condición | Causa | Efecto | Evidencia
   - Hallazgo 2: ...
   - Hallazgo 3: ...
   - (El auditor debe proporcionar; IA solo estructura)

6. **Para evaluación independiente del SCI:**
   - ¿Componentes del SCI evaluados? (5 componentes: ambiente, evaluación de riesgos,
     actividades control, información y comunicación, monitoreo)
   - Evaluación preliminar de madurez por componente (inicial, en desarrollo, definido, optimizado)
   - ¿Existen hallazgos de ejercicios anteriores?

7. **Para seguimiento al PAAC:**
   - ¿Tiene PAAC actual?
   - ¿Cuántos componentes del PAAC se van a evaluar?
   - Avance de las actividades PAAC vs. cronograma previsto
   - Nuevos hallazgos vs. período anterior

8. **Responsable de control interno:**
   - Nombre, cargo, correo, teléfono del jefe de control interno
   - ¿Cuántos profesionales en la oficina?
   - Organización de la función (estructura de equipo)

9. **Plantilla institucional:**
   - ¿Existe plantilla Word con marca, colores, estilos?
   - ¿Debe adherirse a formato específico?
   - Subir archivo si existe

10. **Acceso y distribución:**
    - ¿Informe solo para dirección o también publicación web?
    - ¿Hay supervisores externos (Contraloría, DAFP)?
    - ¿Restricción de información sensible?

### Preguntas opcionales

- ¿Hay plan de auditoría anual establecido?
- ¿Existen indicadores KPI de control interno?
- ¿Se ha hecho evaluación de eficacia del SCI?

---

## Paso 1 — Cuatro modalidades de informe

### Modalidad A: Evaluación Independiente del SCI (Decreto 1499/2017, DAFP)

**Propósito:** Evaluación integral del Sistema de Control Interno conforme a COSO/COSO II

**Estructura:**
```
Portada y Membrete
Índice
Carta de transmisión a DAFP
Ejecutivo: Calificación SCI (Inicial / En desarrollo / Definido / Optimizado)

Sección 1: Metodología de evaluación
├─ Normas aplicadas (COSO, Ley 87/1993, Decreto 1499/2017)
├─ Alcance: Áreas/procesos evaluados
├─ Período: Fechas
├─ Equipo evaluador
└─ Procedimientos aplicados

Sección 2: Componentes del SCI (evaluación por componente)
├─ Componente 1: Ambiente de Control
│  Evaluación: Inicial / En desarrollo / Definido / Optimizado
│  Fortalezas identificadas
│  Debilidades de control interno (= Hallazgos)
│  Recomendaciones
│
├─ Componente 2: Evaluación de Riesgos
│  (estructura similar)
│
├─ Componente 3: Actividades de Control
│  (estructura similar)
│
├─ Componente 4: Información y Comunicación
│  (estructura similar)
│
└─ Componente 5: Monitoreo
   (estructura similar)

Sección 3: Hallazgos (si existen debilidades significativas)
├─ Hallazgo 1: [Criterio | Condición | Causa | Efecto | Evidencia]
│  Recomendación
│  Plan de mejoramiento propuesto
│
└─ Hallazgo 2: ...

Sección 4: Calificación integral del SCI
├─ Puntaje global (Inicial / En desarrollo / Definido / Optimizado)
├─ Comparación con período anterior
└─ Análisis de tendencia

Anexos: Matriz de riesgos, procedimientos, cartas de toma de conocimiento
```

### Modalidad B: Informe Pormenorizado Cuatrimestral (Web pública)

**Propósito:** Reporte de actividades de control durante cuatrimestre, para transparencia

**Estructura:**
```
Portada
Resumen Ejecutivo: N° de auditorías, hallazgos, estado seguimiento

Sección 1: Actividades de Auditoría realizadas
├─ Auditoría 1: [Proceso] [Período] [Responsable] [Estado]
├─ Auditoría 2: ...
└─ Total: N° auditorías planificadas vs. ejecutadas

Sección 2: Hallazgos identificados
├─ Por proceso
├─ Por tipo de hallazgo (Incumplimiento, No conformidad, Debilidad)
├─ Estado de cierre (Abierto, En seguimiento, Cerrado)
└─ Matriz de hallazgos (ver Paso 2)

Sección 3: Seguimiento a hallazgos período anterior
├─ Hallazgos cerrados: N° y temas
├─ Hallazgos en seguimiento: N° y % de implementación
└─ Hallazgos reabiertos (si aplica)

Sección 4: Indicadores de control interno (MIPG Dimensión 7)
├─ % de cobertura de auditoría = (Procesos auditados / Total procesos) × 100
├─ N° de hallazgos por categoría
├─ % de hallazgos cerrados
└─ Tiempo promedio de cierre

Sección 5: Planes de mejoramiento en ejecución
├─ Plan 1: [Descripción] [% Avance] [Plazo]
└─ Plan 2: ...

Anexos: Matriz de hallazgos, contactos
```

### Modalidad C: Seguimiento al PAAC (Cuatrimestral, web pública)

**Propósito:** Verificar implementación de acciones del Plan Anticorrupción

**Estructura:**
```
Portada
Resumen: N° componentes PAAC, N° acciones, % implementación

Sección 1: Estado del PAAC vs. cronograma
├─ Componente 1: Gestión de riesgo
│  ├─ Acción 1.1: [Descripción] [% Avance] [Estado Verde/Amarillo/Rojo]
│  ├─ Acción 1.2: ...
│  └─ Subtotal: X% implementado
│
├─ Componente 2: Racionalización de trámites (SUIT)
│  (estructura similar)
│
├─ Componente 3: Rendición de cuentas
│  (estructura similar)
│
├─ Componente 4: Atención ciudadano
│  (estructura similar)
│
├─ Componente 5: Transparencia
│  (estructura similar)
│
└─ Componente 6: Iniciativas adicionales
   (estructura similar)

Sección 2: Hallazgos en implementación
├─ Hallazgo 1: Retrasos en acción X
│  Causa: ...
│  Recomendación: ...
│
└─ Hallazgo 2: ...

Sección 3: Indicadores de PAAC
│ (ver Skill paac-entidad para detalle)

Anexos: Matriz de seguimiento PAAC, evidencias de avance
```

### Modalidad D: Auditoría Interna de Proceso (Ad hoc)

**Propósito:** Evaluación de conformidad y eficiencia de proceso específico

**Estructura:**
```
Portada
Resumen Ejecutivo: Proceso auditado, período, hallazgos principales, riesgo

Sección 1: Información de la auditoría
├─ Proceso auditado: [Descripción, responsables, importancia]
├─ Período: [Fechas]
├─ Equipo auditor: [Nombres, especialidad]
├─ Criterios: [Normas, políticas, leyes aplicables]
├─ Procedimientos: [Técnicas de auditoría aplicadas]
└─ Limitaciones: [Si existen]

Sección 2: Hallazgos
├─ Hallazgo 1
│  ├─ Criterio: [Norma, política que debería cumplirse]
│  ├─ Condición: [Lo que realmente ocurre]
│  ├─ Causa: [Por qué ocurre]
│  ├─ Efecto: [Impacto en el proceso]
│  └─ Evidencia: [Pruebas documentales]
│
├─ Hallazgo 2: (estructura similar)
│
└─ Hallazgo 3: ...

Sección 3: Conclusiones
├─ Conformidad general del proceso (% de cumplimiento)
├─ Riesgos identificados: Alto / Medio / Bajo
└─ Evaluación de eficiencia: Buena / Regular / Deficiente

Sección 4: Recomendaciones
├─ Recomendación 1 (para cada hallazgo)
├─ Recomendación 2
└─ Recomendación 3

Sección 5: Plan de mejoramiento
├─ Acción 1: [Descripción] [Responsable] [Plazo] [Presupuesto si aplica]
└─ Acción 2: ...

Anexos: Matriz de procedimientos, documentos revisados, entrevistas
```

---

## Paso 2 — Matriz de Hallazgos de Auditoría (elemento clave)

### Estructura de cada hallazgo (IMPRESCINDIBLE)

```
HALLAZGO [N]: [Título descriptivo, máximo 10 palabras]

CRITERIO (¿Qué debería suceder?)
Texto: "Según [Norma/Política/Ley], debe cumplirse que [descripción del requisito]"
Ej: "Según Decreto 1081/2015 Art. 34, los contratos deben ser suscritos por ordenador
    del gasto o su delegatario"

CONDICIÓN (¿Qué observamos realmente?)
Texto: Descripción factual de lo observado durante la auditoría, sin interpretación
Ej: "Se revisaron 20 contratos de 2026. En 5 de ellos (25%) la firma corresponde a
    personal sin competencia legal (asistentes de contratación)"

CAUSA (¿Por qué ocurre la desviación?)
Texto: Análisis de raíz de por qué hay desalineación entre Criterio y Condición
Ej: "La causa es falta de claridad en delegación de facultades. El manual de delegación
    no especifica de forma clara quién suscribe cada tipo de contrato"

EFECTO (¿Cuál es el impacto?)
Texto: Consecuencia o riesgo que genera la incidencia
Ej: "El efecto es riesgo legal: los contratos pueden ser nulos por vicio en la
    formalización, exponiendo a la entidad a litigios y sanciones de Contraloría"

EVIDENCIA (¿Con qué lo probamos?)
Texto: Fuentes documentales que respaldan la condición observada
Ej: "- Contratos No. 001-2026, 003-2026, 008-2026, 015-2026, 019-2026
     - Actas de revisión de firmas (adjuntas)
     - Entrevista con jefe de contratación (15 de marzo de 2026)"

RECOMENDACIÓN (¿Qué debe hacerse?)
Texto: Acción correctiva específica, cuantificable, realizable
Ej: "Actualizar manual de delegación de facultades en 30 días, incluyendo matriz clara
    por tipo de contrato. Capacitar al personal de contratación en nuevos procedimientos"

PLAZO SUGERIDO: [30/60/90 días]
RESPONSABLE: [Cargo específico, ej: Jefe de Contratación]
```

### Tabla resumen de hallazgos

| Hallazgo | Proceso | Categoría | Criterio | Condición resumida | Riesgo | Estado |
|----------|---------|-----------|----------|---|---|---|
| 1 | Contratación | Incumplimiento | Decreto 1081 Art. 34 | Firmas sin competencia | Nulidad contrato | Abierto |
| 2 | Presupuesto | No conformidad | Decreto 1499 Art. 5 | Ejecución sin plan | Desviación presupuestal | Seguimiento |
| 3 | RRHH | Debilidad | Ley 909/2001 | Perfiles no validados | Incompetencia personal | Abierto |

---

## Paso 3 — Roles de Control Interno (Decreto 648/2017)

### 5 Roles que debe evaluar el informe

```
Rol 1: Liderazgo Estratégico
├─ ¿Existe comité de auditoría?
├─ ¿Se reporta directamente a Junta/Consejo?
├─ ¿Hay política de auditoría interna?
└─ Hallazgos si no están cumplidos

Rol 2: Enfoque hacia la Prevención
├─ ¿Se evalúan riesgos antes de que ocurran?
├─ ¿Hay matriz de riesgos institucional?
├─ ¿Control interno forma parte del PAAC?
└─ Hallazgos si es reactivo en lugar de preventivo

Rol 3: Evaluación de la Gestión del Riesgo
├─ ¿Se monitorea matriz de riesgos?
├─ ¿Hay seguimiento a controles de riesgos?
├─ ¿Se incorpora riesgo en decisiones?
└─ Hallazgos de gestión deficiente de riesgos

Rol 4: Evaluación y Seguimiento (Core de auditoría)
├─ ¿Se realizan auditorías según plan?
├─ ¿Se cierran hallazgos de forma oportuna?
├─ ¿Hay matriz de seguimiento actualizada?
└─ Hallazgos de debilidad en seguimiento

Rol 5: Relación con Entes Externos de Control
├─ ¿Hay coordinación con Contraloría?
├─ ¿Se remiten reportes a supervisores sectoriales?
├─ ¿Hay seguimiento a recomendaciones de Contraloría?
└─ Hallazgos si hay desconexión
```

---

## Paso 4 — Indicadores de Control Interno (MIPG Dimensión 7)

### Matriz de indicadores recomendados

| Indicador | Fórmula | Meta | Logrado | % Cumplimiento | Fuente |
|---|---|---|---|---|---|
| Cobertura de auditoría | (Procesos auditados / Total procesos) × 100 | 40% | 35% | 88% | Plan de auditoría |
| Cumplimiento del plan | (Auditorías ejecutadas / Auditorías planificadas) × 100 | 90% | 85% | 94% | Reporte trimestral |
| % Hallazgos cerrados | (Hallazgos cerrados / Total hallazgos abiertos) × 100 | 80% | 75% | 94% | Matriz de seguimiento |
| Tiempo promedio cierre | Promedio de días de cierre de hallazgos | ≤60 días | 65 días | 92% | Matriz seguimiento |
| Efectividad de controles | (Controles preventivos efectivos / Total controles) × 100 | 85% | 78% | 92% | Evaluación auditorías |

---

## Paso 5 — Checklist de conformidad

### Conformidad Ley 87/1993, Decreto 1499/2017 y Decreto 648/2017

- [ ] Tipo de informe claramente especificado (Evaluación SCI / Pormenorizado / PAAC / Auditoría)
- [ ] Período reportado explícitamente indicado
- [ ] Si Evaluación SCI: Los 5 componentes evaluados
- [ ] Matriz de hallazgos con estructura Criterio-Condición-Causa-Efecto-Evidencia
- [ ] Cada hallazgo tiene recomendación específica y plazo
- [ ] Hallazgos clasificados por riesgo (Alto / Medio / Bajo)
- [ ] Seguimiento a hallazgos período anterior (estado de cierre)
- [ ] 5 Roles de control interno evaluados (Decreto 648/2017)
- [ ] Indicadores MIPG Dimensión 7 reportados
- [ ] Responsable de auditoría/control interno identificado (nombre, cargo, correo)
- [ ] Equipo auditor especificado
- [ ] Metodología de auditoría descrita (normas aplicadas)
- [ ] Alcance claramente delimitado (procesos, período, unidades)
- [ ] Conclusión general sobre situación del SCI o proceso
- [ ] Planes de mejoramiento con responsables y plazos
- [ ] Formato .docx con membrete institucional
- [ ] Tabla de contenido automática
- [ ] Trazabilidad de versiones

### Validaciones de contenido

- [ ] No hay hallazgos sin evidencia documentada
- [ ] Causas son análisis de raíz (no interpretaciones subjetivas)
- [ ] Efectos cuantificables o medibles
- [ ] Recomendaciones son accionables (no vagas como "mejorar")
- [ ] Responsables son cargos específicos (no "todos" o "la entidad")
- [ ] Plazos son realistas vs. complejidad de la acción

---

## Paso 6 — Metadatos SGDEA

```
Tipo documental: Informe de Control Interno / Auditoría Interna
Serie: Informes de evaluación institucional
Subserie: [Según modalidad: Evaluación SCI / Auditoría por proceso]
Período: [Fechas, ej: 01 enero 2026 — 30 junio 2026]
Fecha de elaboración: DD/MM/AAAA
Fecha de aprobación por Junta/Consejo: DD/MM/AAAA
Soporte: Electrónico (Word .docx)
Vigencia documental: Permanente (hallazgos de archivo)
Clasificación: Información de control interno (sujeta a protección Art. 12 Ley 1474)
Alineación normativa: Ley 87/1993, Decreto 1499/2017 Dimensión 7, Decreto 648/2017
Responsable de elaboración: Oficina de Control Interno / Jefe de Auditoría
Responsable de aprobación: Junta/Consejo Directivo
Publicación requerida: Sí (modalidades B y C) — Web pública con info. reservada omitida
Periodicidad de actualización: Semestral (SCI) / Cuatrimestral (Pormenorizado, PAAC) / Ad hoc (auditorías)
Acceso: Restricto (liderazgo) o Público parcial (versión para web)
Versión: v01
Distribución interna: Junta/Consejo, Dirección, responsables de procesos auditados
```

---

## Paso 7 — Marco normativo embebido

Ver `references/normativa_transparencia.md` para artículos completos.

**Normas principales:**

- **Ley 87 de 1993** — Sistema de Control Interno
  - Art. 2: Objetivos del control interno
  - Art. 3: Responsables del control

- **Decreto 1499 de 2017** — MIPG Dimensión 7 (Control Interno)
  - Política de control interno
  - Indicadores de evaluación
  - Marcos de madurez (Inicial, En desarrollo, Definido, Optimizado)

- **Decreto 648 de 2017** — Cinco Roles de Control Interno
  - Rol 1: Liderazgo estratégico
  - Rol 2: Enfoque preventivo
  - Rol 3: Evaluación de riesgos
  - Rol 4: Evaluación y seguimiento
  - Rol 5: Relación con entes externos

- **Ley 1474 de 2011** — Estatuto Anticorrupción
  - Art. 75: Confidencialidad de reportes de auditoría interna
  - Artículos 40-42: Medidas disciplinarias por hallazgos

---

## Paso 8 — Notas de uso críticas

### Responsabilidad por la auditoría

```
¿QUÉ HACE ESTA SKILL?
✓ Estructura el informe
✓ Propone campos y formatos
✓ Sintetiza hallazgos basados en info. del auditor
✓ Sugiere categorización de hallazgos
✓ Genera recomendaciones basadas en normas

¿QUÉ NO HACE ESTA SKILL?
✗ Realizar la auditoría en sí (revisión de procesos, validación de evidencia)
✗ Emitir juicio técnico/profesional sobre cumplimiento
✗ Reemplazar a auditor calificado
✗ Tomar muestras ni analizar datos brutos

RESPONSABILIDAD FINAL: El auditor interno / jefe de control interno debe:
• Validar cada hallazgo contra evidencia real
• Asegurar que cause-efecto es correcto
• Completar análisis de raíz
• Obtener respuesta del responsable del proceso
• Aprobar antes de emisión
```

### Diferencia con otros reportes

| Documento | Propósito | Auditor |
|---|---|---|
| Informe de Control Interno | Evaluación de conformidad y riesgo | Auditor interno |
| Rendición de Cuentas | Transparencia a ciudadanía | Personal de planeación |
| PAAC | Estrategia anticorrupción | Comité PAAC |
| Informe de Gestión | Avance de objetivos | Planeación |

### Recomendaciones operativas

1. **Plan de auditoría anual:** Antes de generar informes, definir qué procesos/áreas se van a auditar.

2. **Documentación de evidencia:** Cada hallazgo debe estar respaldado por documentos,
   entrevistas, datos verificables.

3. **Participación de responsables:** Los responsables del proceso deben participar en
   hallazgos (para acuerdos sobre causas y soluciones).

4. **Seguimiento disciplinado:** No cerrar hallazgos sin verificar implementación de
   recomendaciones.

5. **Confidencialidad:** Los informes de auditoría son reservados (Art. 12 Ley 1474).
   Publicar solo versión sanitizada en web.

---

## Paso 9 — Casos de Uso por Modalidad

### Caso 1: Evaluación independiente del SCI (Semestral, DAFP)

Entidad nacional debe reportar a DAFP avance en madurez del SCI. Skill estructura evaluación
conforme a COSO y niveles de madurez MIPG. Auditor valida con instrumentos propios.

### Caso 2: Informe pormenorizado cuatrimestral (Web pública)

Entidad territorial publica cada cuatrimestre resumen de auditorías y hallazgos. Skill genera
estructura clara para transparencia. Información sensible se puede omitir en versión pública.

### Caso 3: Seguimiento al PAAC (Cuatrimestral)

Control interno verifica avance del Plan Anticorrupción vs. cronograma. Skill mapea cada acción
PAAC y reporta estado (verde/amarillo/rojo). Facilita evaluación de cumplimiento de Ley 1474.

### Caso 4: Auditoría interna de proceso (Ad hoc)

Por ejemplo: Auditoría de proceso de Contratación después de hallazgos de Contraloría. Skill
estructura informe de auditoría con hallazgos específicos del proceso (CRITERIO-CONDICIÓN-CAUSA-EFECTO).

---

## MPIA Conformity Block — Acuerdo 003/2025 CDTD, Sección 10

### Sello de conformidad del documento

Incluir al final del documento o en pie de página:

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
AVISO DE USO DE IA — Acuerdo 003/2025 CDTD, Sección 10
Este documento fue elaborado con asistencia de inteligencia artificial
generativa. Su contenido requiere VALIDACIÓN, CORRECCIÓN Y APROBACIÓN
COMPLETA por parte del personal de control interno/auditoría antes de
ser incorporado en comunicaciones, decisiones o actuaciones institucionales.
La IA NO REALIZA LA AUDITORÍA MISMA. El auditor es responsable de
emitir juicio técnico sobre hallazgos y conclusiones.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### Nivel de riesgo MPIA

**MEDIO**

Justificación: El informe de control interno es una evaluación independiente que puede
influir en acciones correctivas, planes de mejoramiento y potencialmente decisiones
disciplinarias. Aunque la auditoría es realizada por personal calificado, la estructuración
del informe por IA requiere validación del jefe de control interno. El riesgo es MEDIO
(no BAJO, porque afecta evaluación de conformidad) pero controlable con revisión humana.

### Metadatos de trazabilidad IA

Incluir en metadatos SGDEA del documento:

```
--- Trazabilidad de uso de IA (Acuerdo 003/2025, Sección 10) ---
Herramienta utilizada: Claude / Skill informe-control-interno-entidad (Cowork)
Tipo de apoyo recibido: Estructuración de informe de auditoría; síntesis de hallazgos
Categoría del sistema de IA: (g) Inteligencia Artificial Generativa
Nivel de riesgo MPIA: Medio
Justificación del nivel: Evaluación independiente que puede influir en acciones
  correctivas. Requiere validación completa por auditor profesional.
Intervención humana requerida: Ejecución de auditoría por personal calificado,
  validación de cada hallazgo, aprobación de jefe de control interno
Fecha de generación: DD/MM/AAAA
Auditor responsable: [Nombre, profesional de auditoría, cédula, matrícula profesional]
Jefe de Control Interno responsable: [Nombre y cargo del aprobador]
```

### Checklist de conformidad MPIA-Bogotá (por documento)

**Conformidad Acuerdo 003/2025 — Sistemas de evaluación de gestión (Sección 10):**

- [ ] El documento es BORRADOR que requiere validación por auditor interno calificado
- [ ] Pie de página con aviso de uso de IA incluido
- [ ] Metadatos de trazabilidad IA incluidos
- [ ] Cada hallazgo validado contra evidencia documentada por auditor
- [ ] Causa-efecto de hallazgos verificados por personal especializado
- [ ] No se ingresaron datos personales sensibles sin protección
- [ ] El contenido NO sustituye auditoría profesional
- [ ] El jefe de control interno revisará, validará y aprobará antes de distribución
- [ ] La aprobación será registrada con firma en acta
- [ ] Para versión pública: se omitió información sensible per Art. 12 Ley 1474

