---
name: informe-gestion-entidad
description: >
  Genera informes de gestión institucionales para entidades del sector público colombiano,
  alineados con el Modelo Integrado de Planeación y Gestión (MIPG). Soporta informes trimestrales,
  semestrales, anuales y de rendición de cuentas. Incluye estructura por dimensiones MIPG,
  indicadores con semáforo, y checklist de conformidad.

  Usar SIEMPRE que alguien pida: informe de gestión, informe trimestral, informe semestral,
  informe anual, rendición de cuentas, balance de gestión, informe de avance, reporte de
  seguimiento, informe de indicadores, informe para el Plan de Acción, informe de supervisión,
  "cómo presentamos los avances", "informe para el comité", "informe para planeación",
  "reporte al DAFP", "informe MIPG", o cualquier variación que implique documentar y reportar
  el avance de gestión de una dependencia o entidad pública colombiana.
---

# Skill: Informe de Gestión — Entidades Públicas Colombia

> Esta skill genera informes de gestión institucional alineados con MIPG.
> Leer `references/normativa_informes.md` para el detalle normativo y las 7 dimensiones MIPG.

---

## Paso 0 — Clasificación y recolección

### Preguntas obligatorias (en una sola interacción)

1. **¿Qué tipo de informe?**
   - Informe de gestión trimestral
   - Informe de gestión semestral
   - Informe de gestión anual
   - Informe de rendición de cuentas (ciudadano)
   - Informe de avance del Plan de Acción
   - Informe de supervisión de contrato
   - Informe para organismo de control
   - Otro (especificar)

2. **Período del informe:** fecha inicio — fecha fin

3. **Entidad y dependencia:** nombre de la entidad, dependencia que reporta, cargo del firmante

4. **Audiencia:**
   - Interno (comité directivo, planeación)
   - Externo (organismo de control, DAFP, ciudadanía)
   - Mixto

5. **Contenido:** ¿Qué logros, actividades, cifras e indicadores debe incluir?
   (puede ser un resumen, notas sueltas, una tabla de datos — la skill los estructura)

6. **¿Tiene indicadores?** (si los tiene, pedir: nombre del indicador, meta, resultado,
   fórmula si aplica)

7. **¿Tiene plantilla institucional?** (archivo .docx)

### Preguntas opcionales
- ¿Se necesita alinear con las dimensiones MIPG? (por defecto: sí para informes de gestión)
- ¿Incluir gráficas? (la skill puede generar gráficas básicas de barras/torta con los datos)
- ¿Hay un Plan de Acción institucional al que se referencian las actividades?
- ¿Destinatario específico? (nombre, cargo)

---

## Paso 1 — Estructura del informe

### Estructura base

```
[MEMBRETE INSTITUCIONAL]

INFORME DE GESTIÓN
[DEPENDENCIA]
[ENTIDAD]

Período: [Mes/Trimestre/Semestre] de [Año]
Fecha de elaboración: [DD de mes de AAAA]

═══════════════════════════════════════════════

TABLA DE CONTENIDO

1. Presentación
2. Contexto institucional
3. Resultados de gestión
   3.1. [Línea estratégica / Dimensión MIPG 1]
   3.2. [Línea estratégica / Dimensión MIPG 2]
   3.N. [...]
4. Indicadores de gestión
5. Dificultades y riesgos
6. Conclusiones y próximos pasos
7. Anexos

═══════════════════════════════════════════════

1. PRESENTACIÓN

El presente informe da cuenta de las actividades desarrolladas y los
resultados alcanzados por [dependencia] de [entidad] durante el período
comprendido entre [fecha inicio] y [fecha fin], en el marco del Plan de
Acción [año] y en cumplimiento de las funciones asignadas mediante
[norma de creación / manual de funciones].

2. CONTEXTO INSTITUCIONAL

[Breve descripción de la entidad, su misión, la dependencia que reporta
y su rol. Máximo 1 párrafo. Si el usuario proporcionó contexto, usarlo;
si no, construirlo con los datos disponibles.]

3. RESULTADOS DE GESTIÓN

[Organizar por líneas estratégicas del Plan de Acción de la entidad o,
si el usuario lo solicita, por las 7 dimensiones del MIPG]
```

### Organización por dimensiones MIPG (si aplica)

Si el usuario solicita alineación MIPG o es un informe para el DAFP, organizar los resultados
según las 7 dimensiones del Modelo Integrado:

| Dimensión | Nombre | Temas asociados |
|---|---|---|
| 1 | Talento Humano | Bienestar, capacitación, clima laboral, meritocracia |
| 2 | Direccionamiento Estratégico y Planeación | Plan estratégico, Plan de Acción, arquitectura institucional |
| 3 | Gestión con Valores para Resultados | Operación por procesos, simplificación de trámites, participación ciudadana |
| 4 | Evaluación de Resultados | Seguimiento, indicadores, planes de mejora |
| 5 | Información y Comunicación | Transparencia, gestión documental, datos abiertos |
| 6 | Gestión del Conocimiento y la Innovación | Lecciones aprendidas, innovación, transferencia |
| 7 | Control Interno | Riesgos, auditorías, planes de mejoramiento |

Para cada dimensión que tenga contenido, usar esta estructura:

```
3.X. DIMENSIÓN [N]: [NOMBRE]

Objetivo estratégico asociado: [Si aplica]

Actividades realizadas:
• [Actividad 1]: [Descripción, resultado, evidencia]
• [Actividad 2]: [Descripción, resultado, evidencia]

Logros destacados:
• [Logro cuantificable con cifra o porcentaje]

Retos identificados:
• [Reto y acción correctiva propuesta]
```

### Sección de indicadores

```
4. INDICADORES DE GESTIÓN

N° | Indicador         | Meta    | Resultado | Avance  | Semáforo
---|-------------------|---------|-----------|---------|----------
1  | [Nombre]          | [Meta]  | [Valor]   | [%]     | [🟢/🟡/🔴]
2  | [Nombre]          | [Meta]  | [Valor]   | [%]     | [🟢/🟡/🔴]

Criterio semáforo:
🟢 Verde:    Avance ≥ 80% de la meta
🟡 Amarillo: Avance entre 50% y 79%
🔴 Rojo:     Avance < 50%
```

Si el usuario proporciona la fórmula del indicador, incluirla debajo de la tabla:
```
Indicador 1: [Fórmula] = [numerador] / [denominador] × 100 = [resultado]%
```

### Secciones finales

```
5. DIFICULTADES Y RIESGOS

[Tabla o lista de las principales dificultades encontradas durante el período,
acciones de mitigación tomadas y estado actual]

N° | Dificultad/Riesgo        | Acción de mitigación     | Estado
---|--------------------------|--------------------------|--------
1  | [Descripción]            | [Qué se hizo]            | [Mitigado/En curso/Pendiente]

6. CONCLUSIONES Y PRÓXIMOS PASOS

[Párrafo de cierre con:]
- Resumen de los principales logros del período
- Porcentaje general de avance (si aplica)
- Actividades priorizadas para el siguiente período
- Necesidades de apoyo o recursos (si aplica)

7. ANEXOS

[Lista de soportes, evidencias o documentos complementarios]

═══════════════════════════════════════════════

Elaboró: [Nombre / Cargo]
Revisó: [Nombre / Cargo]
Aprobó: [Nombre / Cargo — si aplica]

[NOMBRE COMPLETO DEL FIRMANTE]
[Cargo]
[Dependencia]
[Entidad]
```

---

## Paso 2 — Adaptación según audiencia

### Para audiencia interna (comité directivo, planeación)
- Tono técnico y directo
- Incluir cifras detalladas y fórmulas de indicadores
- Incluir tabla de dificultades con acciones correctivas
- Puede ser extenso (sin límite estricto de páginas)

### Para audiencia externa (organismo de control, DAFP)
- Tono institucional y formal
- Incluir referencias normativas de cada actividad
- Alinear explícitamente con dimensiones MIPG
- Incluir evidencias o referencia a soportes

### Para rendición de cuentas (ciudadanía)
- Lenguaje claro y accesible (evitar tecnicismos)
- Incluir cifras de impacto ciudadano
- Gráficas sencillas (barras o torta)
- Máximo 15 páginas
- Usar la "Estrategia de Rendición de Cuentas" del DAFP como referencia

---

## Paso 3 — Adaptación de plantilla

- Si el usuario sube `.docx`: extraer estilos y aplicar
- Si no: formato estándar GTC-185

```
Formato técnico base:
- Tamaño: Carta (21.59 × 27.94 cm)
- Márgenes: Superior 3cm, Inferior 3cm, Izquierdo 3cm, Derecho 2.5cm
- Fuente títulos: Arial 14pt negrita
- Fuente subtítulos: Arial 12pt negrita
- Fuente cuerpo: Arial 11pt
- Fuente tablas: Arial 10pt
- Tablas: bordes simples, encabezado negrita con fondo gris claro
- Tabla de contenido: generada automáticamente con hipervínculos
- Numeración de páginas: inferior derecha, desde la página 2
- Espaciado: 1.15, 6pt entre párrafos
```

Nombre del archivo: `Informe_Gestion_[Dependencia]_[Periodo]_[Año].docx`
Ejemplo: `Informe_Gestion_OCI_Trimestre1_2026.docx`

---

## Paso 4 — Checklist de conformidad

### Conformidad MIPG y normativa
- [ ] Membrete institucional o espacio reservado
- [ ] Período del informe claramente indicado
- [ ] Tabla de contenido presente y coherente con el documento
- [ ] Presentación con contexto institucional
- [ ] Resultados organizados por línea estratégica o dimensión MIPG
- [ ] Cada resultado tiene: actividad, logro cuantificable, evidencia
- [ ] Tabla de indicadores con meta, resultado, avance porcentual y semáforo
- [ ] Sección de dificultades y riesgos con acciones de mitigación
- [ ] Conclusiones con logros del período y próximos pasos
- [ ] Anexos referenciados (si aplica)
- [ ] Firma del responsable
- [ ] Líneas de "Elaboró", "Revisó" y "Aprobó"
- [ ] Tono acorde a la audiencia (técnico / institucional / ciudadano)
- [ ] Si es rendición de cuentas: lenguaje claro, máximo 15 páginas, gráficas

### Metadatos para SGDEA
```
Tipo documental: Informe de Gestión
Serie: Informes
Subserie: [según TRD de la entidad]
Período: [Trimestre/Semestre/Año]
Fecha elaboración: [DD/MM/AAAA]
Folios: [número]
Soporte: Electrónico
Firmante: [Nombre y cargo]
Dependencia: [Nombre]
Alineación MIPG: [Sí/No — Dimensiones cubiertas]
```

---

## Marco normativo embebido

Ver `references/normativa_informes.md` para artículos completos.

**Normas principales:**
- **Decreto 1499/2017** — Adopción del MIPG
- **Manual Operativo MIPG** — DAFP: estructura las 7 dimensiones y políticas de gestión
- **Ley 489/1998** — Organización y funcionamiento de entidades del orden nacional
- **Ley 1712/2014** — Ley de Transparencia: obligación de publicar informes de gestión
- **CONPES 3654/2010** — Política de rendición de cuentas
- **Decreto 612/2018** — Integración de planes institucionales
- **GTC-185** — Formato de documentos

---

## Notas de uso

- **Esta skill NO reemplaza el seguimiento del Plan de Acción.** Si la entidad tiene una
  herramienta de seguimiento (SISGESTION, Strategos, etc.), los datos deben venir de ahí.
- **Indicadores:** Si el usuario no tiene indicadores formulados, la skill puede sugerir
  indicadores tipo basados en las actividades reportadas.
- **Gráficas:** La skill puede generar gráficas básicas (barras, torta) insertadas en el .docx
  usando python-docx. Para gráficas complejas, se recomienda Excel y luego insertar la imagen.
- El informe debe ser validado por el jefe de la dependencia antes de publicación.

---

## Conformidad MPIA-Bogotá — Acuerdo 003/2025 CDTD

### Sello de conformidad del documento

Incluir en el **pie de página** del documento .docx generado:

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
AVISO DE USO DE IA — Acuerdo 003/2025 CDTD, Sección 10
Este documento fue elaborado con asistencia de inteligencia artificial
generativa. Su contenido requiere revisión, corrección y aprobación por
parte del servidor público responsable antes de ser incorporado en
comunicaciones, decisiones o actuaciones institucionales.
La IA no sustituye el juicio técnico, profesional ni ético del funcionario.
El firmante asume la responsabilidad integral sobre el contenido final.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### Metadatos de trazabilidad IA

Incluir en los metadatos SGDEA del documento:

```
--- Trazabilidad de uso de IA (Acuerdo 003/2025, Sección 10) ---
Herramienta utilizada: [Nombre de la plataforma / skill]
Tipo de apoyo recibido: Generación de borrador de documento institucional
Categoría del sistema de IA: (g) Inteligencia Artificial Generativa
Nivel de riesgo MPIA: Bajo
Justificación del nivel: Asistencia en estructuración de informes internos de gestión. Sin decisiones autónomas.
Intervención humana requerida: Revisión, corrección y aprobación completa
Fecha de generación: [DD/MM/AAAA]
Funcionario responsable: [Nombre y cargo del firmante]
```

### Checklist de conformidad MPIA-Bogotá (por documento)

**Conformidad Acuerdo 003/2025 — Uso cotidiano de IA (Sección 10):**
- [ ] El documento es un BORRADOR que requiere aprobación humana (Sección 10)
- [ ] Pie de página con aviso de uso de IA incluido (Numeral 7.5.2.2.4)
- [ ] Metadatos de trazabilidad IA incluidos (Sección 10)
- [ ] No se ingresaron datos personales sensibles, información reservada o clasificada
- [ ] El contenido NO sustituye análisis, interpretación ni deliberación técnica
- [ ] El contenido NO genera actos administrativos ni decisiones vinculantes
- [ ] El funcionario responsable revisará y validará antes de uso institucional

> Para obtener el dictamen completo de conformidad MPIA-Bogotá del proyecto de IA
> de su entidad, utilice la skill `conformidad-mpia-bogota`.
