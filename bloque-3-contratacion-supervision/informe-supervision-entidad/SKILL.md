---
name: informe-supervision-entidad
description: >
  Genera Informes de Supervisión Contractual para contratos públicos en entidades del sector público colombiano,
  conforme a Ley 1474/2011 Arts. 83-85. Incluye estado de ejecución, cumplimiento de obligaciones, análisis
  presupuestal, verificación de pólizas, evaluación de riesgos y concepto favorable/desfavorable para pago.
  Output: .docx profesional con tablas de seguimiento.

  Usar SIEMPRE que alguien pida: informe de supervisión, informe de interventoría, informe de seguimiento
  contractual, supervisión de contrato, reporte de ejecución del contrato, avance de contrato, cumplimiento
  del contratista, estado de la ejecución, verificación de cumplimiento, "cómo va el contrato", concepto para
  pago del contrato, "qué ha entregado el contratista", o cualquier variación sobre monitoreo y evaluación
  de cumplimiento contractual.
---

# Skill: Informe de Supervisión Contractual — Entidades Colombia

> Esta skill genera Informes de Supervisión alineados con Ley 1474/2011 Arts. 83-85 y Decreto 1082/2015.
> Leer `references/normativa_contratacion.md` para referencias normativas completas.
> **ADVERTENCIA:** Este informe es un BORRADOR. Requiere validación técnica y jurídica antes de comunicar
> al contratista o respaldar decisiones de pago/modificación. El supervisor debe mantener evidencia
> de cumplimiento y registrar hallazgos de forma independiente.

---

## Paso 0 — Clasificación y recolección

### Preguntas obligatorias (una sola interacción)

1. **Datos del contrato:**
   - Número de contrato (formato: CDT-AAAA-XXXXX)
   - Objeto del contrato (breve descripción)
   - Contratista (nombre, NIT)
   - Valor del contrato (COP)
   - Fecha de inicio y fecha de finalización

2. **Período del informe:**
   - Fecha inicio del período supervisado
   - Fecha fin del período supervisado
   - ¿Es el informe mensual, trimestral, semestral o final?

3. **Datos del supervisor:**
   - Nombre completo y cargo
   - Dependencia
   - Correo

4. **Estado general del contrato:**
   - ¿El contrato está en ejecución normal, retrasado, en riesgo o finalizado?

5. **¿Tiene plantilla .docx institucional?** (si es sí, cargarla)

### Preguntas técnicas complementarias

6. **Obligaciones principales del contrato:** (máx. 5-7 obligaciones clave)
   - Descripción de cada obligación
   - Fecha de cumplimiento o plazo

7. **Cumplimiento hasta la fecha:**
   - ¿Qué obligaciones se han cumplido? (con evidencia)
   - ¿Qué obligaciones están en proceso? (% avance)
   - ¿Qué obligaciones no se han cumplido? (razones)

8. **Ejecución presupuestal:**
   - Valor presupuestado inicial
   - Valor ejecutado a la fecha
   - % de ejecución presupuestal

9. **Pólizas de cumplimiento:**
   - ¿Está vigente la póliza de cumplimiento?
   - Número de póliza, asegurador, cobertura
   - Fecha de vencimiento

10. **Riesgos identificados:** (técnicos, financieros, administrativos)

11. **¿Se recomida pago? (Sí/No)** y justificación

---

## Paso 1 — Estructura del informe

### Estructura base de Informe de Supervisión

```
[MEMBRETE INSTITUCIONAL]

INFORME DE SUPERVISIÓN CONTRACTUAL

Contrato: [Número]
Objeto: [Descripción breve]
Período: [DD/MM/AAAA] al [DD/MM/AAAA]
Fecha del informe: [DD de mes de AAAA]

═══════════════════════════════════════════════

TABLA DE CONTENIDO

1. Datos del contrato
2. Datos del supervisor
3. Estado de ejecución
4. Cumplimiento de obligaciones
5. Ejecución presupuestal
6. Verificación de pólizas
7. Evaluación de riesgos
8. Hallazgos y observaciones
9. Concepto para pago
10. Recomendaciones
11. Anexos

═══════════════════════════════════════════════

1. DATOS DEL CONTRATO

| Atributo | Valor |
|----------|-------|
| Número de contrato | [CDT-AAAA-XXXXX] |
| Objeto | [Descripción del objeto del contrato] |
| Contratista | [Nombre, NIT] |
| Valor del contrato | $[Cantidad] COP |
| Fecha de inicio | [DD/MM/AAAA] |
| Fecha de finalización | [DD/MM/AAAA] |
| Plazo total | [Número de días o meses] |
| Modalidad | [Vigencias múltiples/Un año/Obra/Servicios/Otro] |

2. DATOS DEL SUPERVISOR

| Atributo | Valor |
|----------|-------|
| Nombre | [Nombre completo] |
| Cargo | [Cargo y nivel] |
| Dependencia | [Nombre de la dependencia] |
| Período de supervisión | [DD/MM/AAAA] al [DD/MM/AAAA] |

3. ESTADO DE EJECUCIÓN

Ejecución general: [Descripción del estado actual del contrato]

Cronograma de ejecución:
| Fase/Hito | Plazo previsto | Plazo real | Estado |
|---|---|---|---|
| [Fase 1] | [Fecha] | [Fecha] | [Cumplido/Retrasado/En proceso] |
| [Fase 2] | [Fecha] | [Fecha] | [Cumplido/Retrasado/En proceso] |

Porcentaje de avance: [X]% del contrato ejecutado

Fundamento normativo: Ley 1474/2011 Art. 83.

4. CUMPLIMIENTO DE OBLIGACIONES

Matriz de cumplimiento de obligaciones contractuales:

| N° | Obligación | Plazo | Cumple | Parcial | No cumple | Evidencia | Observaciones |
|----|---|---|---|---|---|---|---|
| 1 | [Obligación] | [Fecha] | [ ] | [ ] | [ ] | [Soportes] | [Notas] |
| 2 | [Obligación] | [Fecha] | [ ] | [ ] | [ ] | [Soportes] | [Notas] |
| 3 | [Obligación] | [Fecha] | [ ] | [ ] | [ ] | [Soportes] | [Notas] |

Porcentaje de obligaciones cumplidas: [X]%
Porcentaje de obligaciones parcialmente cumplidas: [X]%
Porcentaje de obligaciones incumplidas: [X]%

Fundamento normativo: Ley 1474/2011 Art. 84 (facultades del supervisor).

5. EJECUCIÓN PRESUPUESTAL

| Concepto | Valor |
|----------|-------|
| Presupuesto inicial aprobado | $[Cantidad] COP |
| Ampliaciones/reducciones | $[Cantidad] COP |
| Presupuesto ajustado | $[Cantidad] COP |
| Valor ejecutado a la fecha | $[Cantidad] COP |
| **Porcentaje de ejecución** | **[X]%** |
| Valor pendiente de ejecución | $[Cantidad] COP |

Análisis: [Descripción de si el avance presupuestal es proporcional al avance técnico,
si hay sobreejecución o si hay pagos sin cumplimiento de obligaciones.]

6. VERIFICACIÓN DE PÓLIZAS

Póliza de seriedad de propuesta:
- Número: [XXXX]
- Asegurador: [Nombre]
- Cobertura: $[Cantidad] COP
- Fecha de emisión: [DD/MM/AAAA]
- Fecha de vencimiento: [DD/MM/AAAA]
- Estado: [Vigente/Vencida/No aplica]

Póliza de cumplimiento:
- Número: [XXXX]
- Asegurador: [Nombre]
- Cobertura: [% del valor del contrato o cantidad fija]
- Fecha de emisión: [DD/MM/AAAA]
- Fecha de vencimiento: [DD/MM/AAAA]
- Estado: [Vigente/Vencida/No aplica]

Otras pólizas (responsabilidad civil, amparos específicos):
- [Descripción]
- Estado: [Vigente/Vencida/No aplica]

Observaciones: [Indicar si hay deficiencias en cobertura o vencimientos próximos]

Fundamento normativo: Ley 1474/2011 Arts. 83, 84; Decreto 1082/2015.

7. EVALUACIÓN DE RIESGOS

Matriz de riesgos identificados:

| N° | Tipo de riesgo | Descripción | Probabilidad | Impacto | Acción correctiva |
|----|---|---|---|---|---|
| 1 | Técnico | [Descripción] | Alta/Media/Baja | Alto/Medio/Bajo | [Acción] |
| 2 | Financiero | [Descripción] | Alta/Media/Baja | Alto/Medio/Bajo | [Acción] |
| 3 | Administrativo | [Descripción] | Alta/Media/Baja | Alto/Medio/Bajo | [Acción] |
| 4 | Legal/Normativo | [Descripción] | Alta/Media/Baja | Alto/Medio/Bajo | [Acción] |

Nivel de riesgo general del contrato: [BAJO / MEDIO / ALTO]

8. HALLAZGOS Y OBSERVACIONES

Hallazgos positivos:
• [Aspecto cumplido o sobresaliente]
• [Aspecto cumplido o sobresaliente]

Hallazgos negativos o de mejora:
• [Hallazgo]: [Descripción, impacto, acción solicitada]
• [Hallazgo]: [Descripción, impacto, acción solicitada]

No conformidades identificadas:
[Si las hay, describir si son mayores (riesgo de terminación) o menores (plazo para corregir)]

Cartas enviadas al contratista:
- [Fecha, número de carta, asunto, respuesta recibida]

9. CONCEPTO PARA PAGO

**CONCEPTO: [FAVORABLE / DESFAVORABLE]**

Si es FAVORABLE:
✓ El contratista ha cumplido las obligaciones contractuales
✓ Las pólizas están vigentes y con cobertura suficiente
✓ No hay hallazgos que impidan la ejecución de pagos
✓ Se recomienda autorizar el pago por $[Cantidad] COP

Si es DESFAVORABLE:
✗ El contratista tiene [describir incumplimientos]
✗ Riesgos identificados de nivel [ALTO/CRÍTICO]
✗ Se recomienda NO autorizar pago hasta que:
   - [Condición 1]
   - [Condición 2]
   - [Fecha límite para corrección]

Fundamento normativo: Ley 1474/2011 Art. 84 (opinión del supervisor sobre cumplimiento
y calidad de la prestación es elemento para decisiones de pago).

10. RECOMENDACIONES

- [Recomendación 1 — acción específica para mejorar ejecución o reducir riesgos]
- [Recomendación 2]
- [Recomendación 3]

11. ANEXOS

- Anexo A: Evidencia fotográfica o documental de cumplimiento
- Anexo B: Cartas de observación enviadas al contratista
- Anexo C: Soportes de ejecución presupuestal
- Anexo D: Certificados de las pólizas

═══════════════════════════════════════════════

Elaboró: [Nombre / Cargo de supervisor]
Revisó: [Nombre / Cargo del jefe de dependencia]
Aprobó: [Nombre / Cargo de director o funcionario responsable]

[FIRMA DE SUPERVISOR]
[Nombre completo]
Supervisor del Contrato
[Entidad]
[Fecha]
```

---

## Paso 2 — Adaptación según tipo de contrato

### Contrato de obra pública
- Incluir avance físico (metros ejecutados, fases completadas)
- Verificación de cumplimiento de normas técnicas y de calidad
- Inspección de materiales y acabados
- Registro fotográfico del avance

### Contrato de suministro
- Verificación de cantidad y calidad de bienes entregados
- Inspección de empaque, almacenamiento, entrega
- Cumplimiento de estándares técnicos o certificaciones
- Recepción conforme/no conforme

### Contrato de servicios
- Cumplimiento de estándares de servicio (SLAs)
- Disponibilidad del personal asignado
- Cumplimiento de horarios o jornadas
- Calidad de la prestación reportada

### Contrato de consultoría
- Cumplimiento de entregables (informes, análisis)
- Calidad técnica de los estudios
- Oportunidad en la entrega
- Uso de metodologías acordadas

---

## Paso 3 — Tablas de seguimiento

### Tabla de obligaciones contractuales

Usar esta estructura para cada obligación principal:

| Obligación | Descripción | Plazo | Estado | % Avance | Evidencia |
|---|---|---|---|---|---|
| [Nombre corto] | [Qué debe entregar/hacer] | [Fecha límite] | [Cumplido/Parcial/Incumplido] | [%] | [Documento o acta] |

### Tabla de cumplimiento temporal

Permite ver si el contrato va a tiempo:

| Mes | Actividad planeada | Actividad realizada | % Avance esperado | % Avance real | Brecha |
|----|---|---|---|---|---|
| [Mes] | [Qué debería ocurrir] | [Qué ocurrió] | [%] | [%] | [+/- %] |

---

## Paso 4 — Checklist de conformidad normativa

**Ley 1474/2011 Arts. 83-85:**
- [ ] Supervisor identificado con cargo y dependencia
- [ ] Período de supervisión claramente delimitado
- [ ] Cumplimiento de obligaciones evaluado objetivamente
- [ ] Pólizas verificadas y estado documentado
- [ ] Riesgos identificados y calificados
- [ ] Concepto favorable/desfavorable emitido explícitamente
- [ ] Evidencias de cumplimiento referenciadas
- [ ] Recomendaciones basadas en hallazgos

**Decreto 1082/2015:**
- [ ] Formato de documento conforme
- [ ] Datos del contrato completos
- [ ] Ejecución presupuestal documentada

**General:**
- [ ] Documento es un BORRADOR que requiere validación jurídica
- [ ] NO contiene información clasificada sin protección
- [ ] Todos los anexos están referenciados
- [ ] Firma del supervisor autentifica el informe
- [ ] Tono profesional, objetivo, basado en evidencia

---

## Metadatos SGDEA

```
Tipo documental: Informe de Supervisión Contractual
Serie: Supervisión
Subserie: Informes de supervisión
Período: [Mes/Trimestre/Vigencia]
Fecha elaboración: [DD/MM/AAAA]
Folios: [número]
Soporte: Electrónico
Firmante: [Nombre y cargo de supervisor]
Dependencia: [Nombre]
Número de contrato: [CDT-AAAA-XXXXX]
Valor del contrato: [COP]
Contratista: [Nombre, NIT]
```

---

## Marco normativo embebido

Ver `references/normativa_contratacion.md` para artículos completos.

**Normas principales:**
- **Ley 1474/2011** — Estatuto Anticorrupción (Arts. 83-85: supervisión e interventoría)
- **Decreto 1082/2015** — Decreto Único (contratación pública, formatos)
- **Ley 594/2000** — Gestión documental y conservación
- **Ley 80/1993** — Estatuto General de Contratación (principios, responsabilidades)

---

## Notas de uso

- **Esta skill NO reemplaza el seguimiento técnico del contrato.** El supervisor debe mantener
  registros independientes de inspecciones, cartas, evidencias fotográficas.
- **Evidencia:** Cada afirmación sobre cumplimiento debe tener evidencia soportada
  (actas de recepción, cartas del contratista, certificados, fotografías).
- **Concepto para pago:** El concepto favorable NO es aprobación automática de pago.
  La Entidad Contratante mantiene autonomía para decidir si paga.
- **Responsabilidad:** El supervisor responde disciplinaria, fiscal y penalmente por
  negligencia en supervisión o por autorizar pagos sin cumplimiento (Ley 1474/2011 Art. 85).
- **Frecuencia:** Se recomienda informe mensual para contratos de valor alto o riesgo medio,
  y trimestral para contratos de menor cuantía.

---

## Conformidad MPIA-Bogotá — Acuerdo 003/2025 CDTD

### Sello de conformidad del documento

Incluir en el **pie de página** del .docx:

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
DOCUMENTO ASISTIDO POR IA — Acuerdo 003/2025 CDTD, Sección 10
Este informe fue estructurado con asistencia de inteligencia artificial generativa.
Requiere revisión y validación completa por el supervisor responsable antes de uso.
La IA NO sustituye inspección técnica, análisis independiente ni documentación de
hallazgos. El supervisor mantiene responsabilidad integral sobre el contenido.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### Metadatos de trazabilidad IA

```
--- Trazabilidad IA (Acuerdo 003/2025, Sección 10) ---
Herramienta: Skill Cowork — Supervisión Contractual
Tipo de apoyo: Estructuración de informe de supervisión
Categoría IA: (g) Inteligencia Artificial Generativa
Nivel de riesgo MPIA: MEDIO
Justificación: El informe de supervisión puede influir en decisiones de pago y modificación
contractual, pero el supervisor mantiene capacidad de verificación independiente.
Intervención humana: REQUERIDA — Validación de hallazgos y concepto por supervisor
Fecha de generación: [DD/MM/AAAA]
Funcionario responsable: [Nombre y cargo del supervisor]
```

### Checklist de conformidad MPIA-Bogotá

- [ ] Riesgo MEDIO documentado
- [ ] Pie de página con advertencia incluido
- [ ] Metadatos de trazabilidad IA incluidos
- [ ] NO se ingresaron datos personales sensibles
- [ ] El documento es BORRADOR que requiere validación del supervisor
- [ ] Concepto se basa en evidencia documentada
- [ ] Supervisor asume responsabilidad integral
- [ ] Hallazgos están soportados y referenciados

> Para obtener dictamen MPIA completo, utilice la skill `conformidad-mpia-bogota`.
