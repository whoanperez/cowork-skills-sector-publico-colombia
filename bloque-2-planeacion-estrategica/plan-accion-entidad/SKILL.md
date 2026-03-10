---
name: plan-accion-entidad
description: >
  Genera planes de acción institucionales para entidades del sector público colombiano,
  alineados con el Modelo Integrado de Planeación y Gestión (MIPG) y el Plan de Desarrollo
  vigente. Integra los 12 planes estratégicos de Decreto 612/2018, estructura jerárquica
  (objetivo → estrategia → programa → proyecto/actividad), indicadores con semáforo de
  avance, presupuesto, responsables y cronograma. Soporta vigencia nacional y territorial.
  Output en formato Excel (.xlsx) con seguimiento cuantitativo.

  Usar SIEMPRE que alguien pida: plan de acción, plan operativo anual, POA, plan de
  actividades, plan de trabajo institucional, planificación del año, alineación con el
  plan de desarrollo, integración de planes Decreto 612, plan de mejora con presupuesto,
  "cómo estruturamos el plan", "plan con indicadores y semáforo", "plan de acción MIPG",
  "plan alineado con PDD", o cualquier variación que implique crear o actualizar un plan
  de acción institucional con seguimiento operativo.
---

# Skill: Plan de Acción — Entidades Públicas Colombia

> Esta skill genera planes de acción institucionales en Excel (.xlsx), alineados con MIPG,
> Decreto 612/2018 e integrados con el Plan de Desarrollo territorial/nacional vigente.
> Leer `references/normativa_planeacion.md` para el detalle normativo, las 7 dimensiones
> MIPG y los 12 planes estratégicos obligatorios.

---

## Paso 0 — Clasificación y recolección

### Preguntas obligatorias (en una sola interacción)

1. **Tipo de entidad:**
   - Entidad de orden nacional (ministerios, departamentos administrativos, unidades especiales)
   - Entidad territorial (gobernación, municipio, distrito)
   - Entidad descentralizada (instituto, empresa pública, fondo)
   - Otro (especificar)

2. **Vigencia del plan:** año(s) que cubre (ej: 2026, 2026-2030, 2024-2027)

3. **Plan de Desarrollo vigente:**
   - ¿Existe PDD (Plan de Desarrollo Distrital/Municipal/Departamental) o PDN (Plan Nacional de Desarrollo)?
   - ¿Cuál es el nombre exacto?
   - ¿Tiene disponible el documento en PDF o enlace?
   - ¿Cuáles son los ejes/pilares principales? (máximo 5)

4. **Estructura del plan:**
   - ¿Cuántos objetivos estratégicos tiene la entidad?
   - ¿Tiene líneas estratégicas o dimensiones MIPG como marco?
   - ¿Prefiere estructura por líneas temáticas o por dimensiones MIPG (7 dimensiones)?
   - Objetivo general del plan (máximo 1-2 párrafos)

5. **Desagregación temporal:**
   - ¿Desglosen anual?
   - ¿Desglosen trimestral?
   - ¿Desglosen semestral?
   - (Define las filas de la columna "Timeline")

6. **Planes integrados Decreto 612/2018:**
   - ¿La entidad tiene obligación de integrar los 12 planes? (gobernación, municipio, orden nacional → SÍ)
   - ¿Algunos de los 12 planes ya existen y deben vincularse?
   - Lista de planes que tiene (ej: Plan de Gestión Ambiental, Plan de Gestión de Talento Humano, etc.)

7. **Indicadores:**
   - ¿Tiene indicadores ya formulados por objetivo/programa/proyecto?
   - ¿Hay metas por período (anual, trimestral)?
   - ¿Tiene fórmulas de indicadores o solo nombres?

8. **Presupuesto:**
   - ¿Tiene presupuesto global asignado al plan?
   - ¿Hay distribución por programa, proyecto o línea?
   - ¿En qué formato? (total, anual, trimestral, por rubro)

9. **Responsables:**
   - ¿Quién es el responsable de cada objetivo estratégico? (cargo/dependencia)
   - ¿Cada programa/proyecto tiene responsable específico?
   - ¿Hay equipo multidisciplinario?

10. **Plantilla institucional:**
    - ¿Tiene plantilla .xlsx institucional que deba respetarse?
    - ¿Hay estilos, colores o estructura mandatoria?
    - Si es sí: subir archivo

### Preguntas opcionales
- ¿Hay riesgos o supuestos asociados a cada objetivo/programa?
- ¿Desea incluir una columna de "% Ejecución" separada de "% Avance"?
- ¿Necesita un sheet adicional para "Articulación con PDD"?
- ¿Incluir semáforo con reglas de formato condicional?
- ¿Necesita matriz de trazabilidad (Misión → Visión → Objetivos estratégicos)?

---

## Paso 1 — Estructura del documento Excel

### Estructura jerárquica (niveles)

```
Nivel 1: Objetivo Estratégico
         ↓ Alineado a dimensión MIPG + política MIPG + eje PDD

Nivel 2: Estrategia
         ↓ Cómo se alcanza el objetivo (enfoque, metodología)

Nivel 3: Programa
         ↓ Conjunto de actividades interrelacionadas

Nivel 4: Proyecto / Actividad
         ↓ Acción específica con responsable, presupuesto, plazo

Nivel 5: Indicador
         ↓ Métrica de cumplimiento con meta y seguimiento
```

### Sheets del libro Excel

**Sheet 1: Plan de Acción Integral**
- Columnas base: [ver Paso 2]
- Filas: Nivel de detalle según desagregación (anual o trimestral)
- Estilos: Encabezados en negrita, filas alternadas, semáforo con color

**Sheet 2: Planes Integrados Decreto 612**
- Matriz de los 12 planes estratégicos obligatorios
- Mapeo a objetivos del Plan de Acción
- Estado de formulación (Formulado, En formulación, No aplica)
- Referencia cruzada con la hoja principal

**Sheet 3: Matriz de Indicadores**
- Indicador | Meta anual | Meta período | Fórmula | Línea base | Responsable | Periodicidad seguimiento

**Sheet 4: Articulación PDD [Opcional]**
- Eje/Pilar PDD | Objetivo Institucional | Programa | Indicador | Meta PDD | Meta entidad | Brecha
- Permite visualizar alineación con el plan territorial

**Sheet 5: Presupuesto por Programa [Si aplica]**
- Programa | Proyecto | Presupuesto asignado | Presupuesto ejecutado | % Ejecución | Variación

**Sheet 6: Glosario y referencias**
- Definiciones de términos clave (Objetivo, Estrategia, Programa, etc.)
- Referencias normativas (Decreto 1499/2017, Decreto 612/2018, etc.)
- Contactos de responsables

### Columnas de Sheet 1 (Plan de Acción Integral)

```
A. Dimensión MIPG (1-7)
   Valores: Talento Humano | Direccionamiento Estratégico | Gestión con Valores |
   Evaluación de Resultados | Información y Comunicación | Gestión del Conocimiento |
   Control Interno

B. Política MIPG (nombrada según Manual Operativo MIPG)
   Ej: "Política de Competitividad y Productividad"

C. Eje / Pilar PDD
   Ej: "Bogotá Positiva", "Crecimiento Económico", "Seguridad"

D. Objetivo Estratégico [Nivel 1]
   Formato: "Mejorar la capacidad de X en Y%" o "Implementar X para lograr Y"

E. Estrategia [Nivel 2]
   Cómo: "A través de", "Mediante", "Por medio de"

F. Programa [Nivel 3]
   Conjunto de actividades relacionadas

G. Proyecto / Actividad [Nivel 4]
   Acción específica, concreta, ejecutable

H. Indicador (nombre)
   Ej: "% de personas capacitadas", "Número de procesos digitalizados"

I. Fórmula del indicador
   Ej: "(Personas capacitadas / Personas meta) × 100"

J. Meta del período (anual, trimestral según Paso 0 Q5)
   Valor numérico o %

K. Avance (última actualización)
   Valor actual reportado

L. % Avance
   = (Avance / Meta del período) × 100
   Fórmula Excel: =K/J*100

M. Semáforo
   Fórmula: IF(L>=80, "Verde", IF(L>=50, "Amarillo", "Rojo"))
   Formato condicional: Verde (RGB 0,176,80), Amarillo (RGB 255,192,0), Rojo (RGB 255,0,0)

N. Presupuesto asignado (COP)
   Numérico, formato moneda

O. Presupuesto ejecutado (COP)
   Numérico, formato moneda

P. % Ejecución presupuestal
   = (O / N) × 100

Q. Responsable (cargo/dependencia)
   Ej: "Director de Planeación", "Subdirección de Talento Humano"

R. Correo responsable (opcional)
   Para facilitar contacto

S. Fecha inicio (YYYY-MM-DD)
   Formato fecha

T. Fecha fin (YYYY-MM-DD)
   Formato fecha

U. Observaciones / Notas
   Campo libre para aclaraciones, riesgos, supuestos

```

---

## Paso 2 — Adaptación del plan según tipo de entidad

### Para entidades de orden nacional

- **Horizonte:** Generalmente vigencia anual (un año calendario)
- **Referencia:** Plan Nacional de Desarrollo (PDN) de Presidencia / DNPM
- **Planes integrados:** Todos los 12 planes de Decreto 612/2018 (obligatorio)
- **Nivel de detalle:** Por programa y proyecto, con responsables por dependencia
- **Presupuesto:** CGRF, CONPES, marco de gasto de mediano plazo (MGPM)

**Ejemplo de estructura:**
```
Objetivo estratégico 1: Fortalecer la capacidad de atención integral a ciudadanía
  ├─ Estrategia 1.1: Modernización de canales de atención
  │   ├─ Programa 1.1.1: Transformación digital
  │   │   ├─ Proyecto 1.1.1.1: Implementación de portal único de trámites
  │   │   └─ Proyecto 1.1.1.2: Capacitación en nuevas plataformas
  │   └─ Programa 1.1.2: Mejora de atención presencial
  └─ Estrategia 1.2: Fortalecimiento de talento humano
      └─ Programa 1.2.1: Plan de capacitación continua
```

### Para gobiernos territoriales (gobernación, municipio, distrito)

- **Horizonte:** Generalmente 4 años (correspondiente al periodo del gobernante)
- **Referencia:** Plan de Desarrollo Territorial (PDT) — Ley 152/1994
- **Planes integrados:** Todos los 12 planes de Decreto 612/2018 (obligatorio)
- **Nivel de detalle:** Por programa y proyecto con perspectiva de resultados
- **Cronograma:** Desagregación anual mínimo (cuatrimestral preferible)
- **Coordinación:** Articulación con planes sectoriales (Educación, Salud, etc.) y EOTS/EMPALMES

**Ejemplo de estructura (Municipio):**
```
Eje 1 del PDD: Bogotá Positiva
  ├─ Objetivo institucional 1: Ampliar la cobertura educativa
  │   ├─ Estrategia 1.1: Construcción y mejora de infraestructura educativa
  │   │   ├─ Programa: Colegios del siglo XXI
  │   │   │   ├─ Proyecto 1: Construcción colegio zona 1 (2026-2027)
  │   │   │   └─ Proyecto 2: Mejoramiento colegio zona 2 (2026)
  │   │   └─ Programa: Acceso a educación técnica
  │   │       └─ Actividad: Alianzas SENA-Municipio
  │   └─ Estrategia 1.2: Fortalecimiento pedagógico y de gestión
  │       └─ Programa: Capacitación docentes
  │           └─ Actividad: Diplomado en competencias digitales
  └─ Objetivo institucional 2: Mejorar indicadores de cobertura en servicios básicos
```

### Para entidades descentralizadas e institutos

- **Horizonte:** Según estatutos (usualmente 1-4 años)
- **Referencia:** Contrato-plan con entidad adscrita + objetivos institucionales propios
- **Planes integrados:** Solo los 12 planes relevantes para su naturaleza
- **Estructura:** Por línea misional y línea de administración

---

## Paso 3 — Integración de Decreto 612/2018 (12 planes estratégicos)

El Decreto 612/2018 (Del Gobierno Nacional) ordena integrar 12 planes estratégicos
en el Plan de Acción institucional. Estos son:

| # | Plan | Normativa | Aplica a |
|---|------|-----------|----------|
| 1 | Plan de Gestión de Talento Humano | Decreto 1499/2017 | Todas |
| 2 | Plan de Comunicación Pública | Ley 1712/2014 + Resolución MINTIC | Todas |
| 3 | Plan de Gestión Ambiental | Ley 99/1993, Decreto 1299/2008 | Todas (con énfasis territorial) |
| 4 | Plan de Modernización e Innovación | Decreto 1499/2017 | Todas |
| 5 | Plan de Gestión de Tecnología e Información | Decreto 1499/2017, CONPES 4173 | Todas |
| 6 | Plan de Gestión del Riesgo | Ley 1523/2012 | Todas (obligatorio para territoriales) |
| 7 | Plan de Gestión de Seguridad de la Información | Decreto 2693/2012 | Todas |
| 8 | Plan de Transparencia y Acceso a la Información Pública | Ley 1712/2014 | Todas |
| 9 | Plan de Gestión de Archivos | Ley 594/2000 | Todas |
| 10 | Plan de Igualdad, Inclusión y No Discriminación | Decreto 4070/2011 | Todas |
| 11 | Plan de Adquisiciones Sostenibles | Decreto 1081/2015 | Todas |
| 12 | Plan de Auditoría Interna | Ley 87/1993, Decreto 1537/2001 | Todas |

**En Sheet 2 (Planes Integrados Decreto 612):**

```
Plan | Responsable | Vigencia | Estado | Articulación con Plan de Acción | Objetivo asociado
-----|-------------|----------|--------|--------------------------------|-----------------
1. Gestión de Talento Humano | RRHH | 2026 | Formulado | Sí — Objetivo 3 | Mejorar clima laboral
2. Comunicación Pública | Comunicaciones | 2026 | Formulado | Sí — Objetivo 5 | Transparencia
...
```

### Criterios de articulación

- Cada plan estratégico debe estar vinculado a al menos UN objetivo del Plan de Acción
- Si un plan NO está alineado, indicar si es por:
  - [ ] Aún en formulación
  - [ ] No aplica a la entidad
  - [ ] En revisión
  - [ ] Será integrado en siguiente versión

---

## Paso 4 — Configuración de semáforo y seguimiento

### Criterios de semáforo de avance

```
🟢 VERDE:     % Avance ≥ 80%
  → Actividad en buen ritmo. Mantener o acelerar.

🟡 AMARILLO:  % Avance entre 50% y 79%
  → Actividad con retrasos moderados. Revisión de riesgos y plan de recuperación.

🔴 ROJO:      % Avance < 50%
  → Actividad en riesgo. Acción inmediata, replanteamiento o reasignación de recursos.
```

### Fórmula en Excel (Columna M)

```excel
=IF(L1>=0.80, "Verde", IF(L1>=0.50, "Amarillo", "Rojo"))
```

### Formato condicional en Excel

```
Columna M (Semáforo):
  ├─ Condición 1: Si valor = "Verde" → Color fondo RGB(0,176,80), texto blanco
  ├─ Condición 2: Si valor = "Amarillo" → Color fondo RGB(255,192,0), texto negro
  └─ Condición 3: Si valor = "Rojo" → Color fondo RGB(255,0,0), texto blanco
```

### Integración con semáforo presupuestal (opcional)

Columna P (% Ejecución presupuestal) puede tener mismo criterio:
```excel
=IF(P1>=0.80, "Verde", IF(P1>=0.50, "Amarillo", "Rojo"))
```

Esto permite ver si retraso es por cuestiones operativas (avance) o presupuestales (ejecución).

---

## Paso 5 — Temporalidad: desagregación anual vs trimestral

### Opción A: Desagregación anual (para planes de corto plazo o nacionales)

```
Columna T: Fecha inicio (YYYY-MM-DD)
Columna U: Fecha fin (YYYY-MM-DD)
Columna J: Meta del período = Meta anual
Columna K: Avance = Acumulado del año
```

Estructura: Una fila por proyecto/actividad. Actualización mínimo trimestral.

### Opción B: Desagregación trimestral (para territorios con horizonte 4 años)

```
Filas múltiples por proyecto:
  Fila 1: Proyecto X — Trimestre 1 de 2026
  Fila 2: Proyecto X — Trimestre 2 de 2026
  Fila 3: Proyecto X — Trimestre 3 de 2026
  Fila 4: Proyecto X — Trimestre 4 de 2026
  Fila 5: Proyecto X — Trimestre 1 de 2027
  ...

Columna T: Trim_1, Trim_2, Trim_3, Trim_4 (o rango de fechas)
Columna J: Meta trimestral
Columna K: Avance trimestral
```

**Ventaja:** Mayor granularidad para detectar desviaciones temprano.
**Desventaja:** Mayor volumen de datos.

### Opción C: Desagregación semestral

Intermedia. Aplicable para horizontes 2-3 años.

---

## Paso 6 — Plantilla institucional y formato

### Si el usuario NO proporciona plantilla

Usar formato estándar corporativo GTC-185:

```
Libro: Plan_Accion_[NombreEntidad]_[Vigencia].xlsx
Estilos base:
├─ Encabezados (Row 1): Arial 11pt negrita, fondo gris RGB(192,192,192)
├─ Subencabezados (Objetivos): Arial 11pt negrita, fondo azul claro RGB(217,225,242)
├─ Filas de datos: Arial 10pt, alternancia gris RGB(242,242,242) cada 2 filas
├─ Ancho columnas: automático según contenido (máx 30 caracteres antes de ajuste)
├─ Bordes: Simples, RGB(128,128,128)
├─ Congelación: Row 1 (encabezado congelado para scroll vertical)
└─ Zoom por defecto: 85% (para visualizar 10+ columnas)
```

**Colores temáticos por dimensión MIPG (fila de agrupación):**
```
Dimensión 1 (Talento Humano): Verde oscuro RGB(0,100,0)
Dimensión 2 (Direccionamiento Estratégico): Azul oscuro RGB(0,51,102)
Dimensión 3 (Gestión con Valores): Naranja RGB(204,102,0)
Dimensión 4 (Evaluación de Resultados): Rojo oscuro RGB(102,0,0)
Dimensión 5 (Información y Comunicación): Púrpura RGB(102,51,153)
Dimensión 6 (Gestión del Conocimiento): Turquesa RGB(0,153,153)
Dimensión 7 (Control Interno): Marrón RGB(102,76,51)
```

### Si el usuario proporciona plantilla .xlsx

- Respetar estilos, colores, encabezados
- Ajustar estructura de columnas al máximo 5 columnas de diferencia
- Mantener el logo/membrete si está en la esquina superior izquierda
- Preservar cualquier hoja adicional existente

---

## Paso 7 — Articulación con Plan de Desarrollo (PDD/PDN)

### Sheet 4: Matriz de Articulación (OPCIONAL — si usuario proporciona PDD)

Crear tabla de correspondencia:

```
Eje PDD | Objetivo PDD | Objetivo Institucional | Programa | Indicador | Meta PDD | Meta entidad | % Alineación
--------|--------------|------------------------|----------|-----------|----------|--------------|---------------
Eje 1 | Obj 1.1 | Objetivo 1 | Prog 1.1 | Indicador 1 | 80% | 85% | 106%
```

**Beneficios:**
- Permite supervisión territorial (gobernación/municipio) validar alineación
- Evidencia articulación ante DNPM, DAFP o control territorial
- Detecta "brechas de plan" (objetivos institucionales SIN articulación con PDD)

**Advertencia:** Si hay objetivos sin articulación, preguntar al usuario:
- ¿Es un objetivo autónomo de la entidad? (ej: gestión interna)
- ¿Falta alineación? (riesgo de desalineación institucional)

---

## Paso 8 — Checklist de conformidad

### Conformidad MIPG, Decreto 612/2018 y normativa

- [ ] Libro Excel con al menos 2 sheets (Plan principal + Planes Decreto 612)
- [ ] Dimensión MIPG especificada para cada objetivo (A)
- [ ] Política MIPG asociada a cada dimensión (B)
- [ ] Eje/Pilar del PDD referenciado (si aplica) (C)
- [ ] Estructura jerárquica clara: Objetivo → Estrategia → Programa → Proyecto (D-G)
- [ ] Indicadores con fórmula explícita (H-I)
- [ ] Metas del período (anual, trimestral) cuantificables (J)
- [ ] Columna de avance con cálculo automático (K-L)
- [ ] Semáforo con formato condicional RGB (M)
- [ ] Presupuesto asignado y ejecutado con % (N-P)
- [ ] Responsable claro por cada proyecto (Q)
- [ ] Cronograma con fechas inicio y fin (S-T)
- [ ] Hoja de "Planes Integrados Decreto 612" con 12 planes mapeados (Sheet 2)
- [ ] Hoja de "Matriz de Indicadores" con fórmulas (Sheet 3)
- [ ] [Si aplica] Hoja de "Articulación PDD" (Sheet 4)
- [ ] Glosario y referencias normativas (Sheet final)
- [ ] Congelación de encabezado (Row 1)
- [ ] Alternancia de colores en filas para legibilidad

### Validaciones de datos

- [ ] No hay celdas vacías en columnas obligatorias (A-T)
- [ ] Metas numéricas en columnas J, K, L, N, O, P
- [ ] Fechas en formato YYYY-MM-DD (S, T)
- [ ] Fórmulas en L y P recalculadas automáticamente
- [ ] Semáforo en M actualiza al cambiar L
- [ ] Responsables con cargo y/o dependencia identificables
- [ ] No hay duplicados de proyectos/actividades en columna G

### Metadatos para SGDEA

```
Tipo documental: Plan de Acción / Plan Operativo Anual (POA)
Serie: Planes estratégicos
Subserie: [según TRD de la entidad]
Período: [Año o rango de años, ej: 2026-2030]
Fecha elaboración: [DD/MM/AAAA]
Soporte: Electrónico (Excel .xlsx)
Vigencia: [2026] o [2026-2030]
Alineación MIPG: Sí — [Dimensiones cubiertas, ej: todas 7]
Decreto 612: Sí — [12 planes integrados en Sheet 2]
Articulación PDD: [Sí/No]
Responsable de seguimiento: [Nombre y cargo — usualmente Planeación]
Periodicidad de actualización: [Trimestral / Semestral / Anual]
Acceso: [Interno / Restringido / Público]
```

---

## Paso 9 — Guía paso a paso de generación

### Fase 1: Recolección (usuario)
1. Usuario responde Paso 0 (11 preguntas obligatorias)
2. Usuario carga PDD (si existe) — PDF o enlace
3. Usuario carga plantilla institucional .xlsx (si existe)
4. Usuario proporciona listado de objetivos estratégicos, programas, proyectos (puede ser borrador)

### Fase 2: Estructuración (skill)
1. Skill analiza PDD y extrae ejes/pilares principales
2. Skill organiza objetivos y programas en estructura jerárquica
3. Skill asigna dimensiones MIPG a cada objetivo
4. Skill crea libro Excel con estructura base (todas las columnas A-U)
5. Skill rellena con datos del usuario (formulario de Paso 0)

### Fase 3: Indicadores y fórmulas
1. Si usuario tiene indicadores: Skill los ingresa en columnas H-I
2. Si usuario NO tiene indicadores: Skill sugiere 2-3 indicadores por programa
3. Skill inserta fórmulas automáticas en columnas L (% Avance) y P (% Ejecución)
4. Skill configura semáforo con formato condicional en columna M

### Fase 4: Integración Decreto 612
1. Skill crea Sheet 2 con los 12 planes
2. Skill pregunta al usuario por estado de cada plan (Formulado / En formulación / No aplica)
3. Skill sugiere articulación de cada plan con objetivos del Plan de Acción

### Fase 5: Acabado y validación
1. Skill congela encabezados (Row 1)
2. Skill aplica estilos (colores, bordes, ajuste automático)
3. Skill inserta tabla de glosario en última hoja
4. Skill genera resumen ejecutivo (hoja de portada opcional)

### Fase 6: Entrega
1. Archivo descargable: `Plan_Accion_[Entidad]_[Vigencia].xlsx`
2. Metadatos SGDEA incluidos en Sheet de Glosario
3. Instrucciones para actualización y seguimiento adjuntas

---

## Paso 10 — Notas de uso y recomendaciones

### Conexión con Informe de Gestión

- **El Plan de Acción es la fuente de verdad operativa.** El Informe de Gestión trimestral/anual
  reporta el avance del Plan de Acción.
- La columna K (Avance) del Plan se actualiza con periodicidad (trimestral, semestral, anual)
  según ciclo de seguimiento de la entidad.
- Para generar informe trimestral, usar datos del Plan de Acción del período correspondiente
  (usar skill `informe-gestion-entidad`).

### Revisión de metas realistas

- Las metas en columna J deben ser **SMART**: Específicas, Medibles, Alcanzables, Relevantes, con Tiempo.
- Si una meta tiene % Avance consistentemente >120%, revisar si es muy baja (riesgo de complacencia).
- Si una meta tiene % Avance consistentemente <30%, revisar si es inalcanzable (riesgo de desmoralización).

### Gestión de cambios

- Si hay cambios en el objetivo, estrategia o programa: **NO eliminar filas, sino versionar.**
  (Usar columna "Observaciones" para anotar cambios)
- Mantener histórico de avances para análisis de tendencias.
- Cada cambio debe registrarse con fecha y responsable.

### Riesgos comunes

1. **Metas muy amplias:** Proyecto con 20+ actividades en una sola fila.
   Solución: Desagregar en sub-proyectos (filas adicionales).

2. **Indicadores sin fórmula:** Métrica vaga como "Mejorar eficiencia".
   Solución: Formulación explícita: "(Trámites procesados / Tiempo promedio) × 100"

3. **Desalineación con PDD:** Objetivos institucionales sin conexión al plan territorial.
   Solución: Usar Sheet 4 (Articulación) para validar con Planeación municipal/departamental.

4. **Presupuesto no asignado:** Proyectos sin presupuesto (columna N vacía).
   Solución: Coordinar con Hacienda/Finanzas para asignación o reclasificar como "sin costo" (0).

5. **Responsables difusos:** "Todas las áreas" en columna Q.
   Solución: Designar responsable principal + equipo de apoyo en "Observaciones".

---

## Marco normativo embebido

Ver `references/normativa_planeacion.md` para artículos completos.

**Normas principales:**

- **Decreto 1499/2017** — Adopción del Modelo Integrado de Planeación y Gestión (MIPG)
  - Establece las 7 dimensiones de gestión pública
  - Define políticas de gestión institucional

- **Decreto 612/2018** — Integración de los planes estratégicos de la Administración Pública
  - Ordena integrar 12 planes en el Plan de Acción
  - Aplica a todas las entidades del orden nacional y territorial

- **Ley 152/1994** — Ley Orgánica del Plan de Desarrollo
  - Marco legal para planes de desarrollo (PDN, PDD)
  - Estructura y procedimiento de planes estratégicos

- **Ley 489/1998** — Ley de Organización y Funcionamiento de la Administración Pública
  - Artículos 29, 33: Obligación de planeación anual
  - Seguimiento y evaluación de planes

- **Ley 1712/2014** — Ley de Transparencia y Acceso a la Información Pública
  - Publicación de planes y avances

- **GTC-185** — Guía Técnica Colombiana para documentación de sector público
  - Formato y estructura estándar de documentos

---

## Ejemplo de uso completo

**Caso: Municipio de Bogotá, Secretaría de Educación, vigencia 2026**

### Entrada (Paso 0)
1. Tipo de entidad: Entidad territorial (Municipio)
2. Vigencia: 2026
3. PDD: "Bogotá Positiva 2024-2028" — Eje 1: Educación inclusiva y de calidad
4. Objetivos estratégicos: 3
5. Desagregación: Trimestral
6. Planes Decreto 612: Sí, todos
7. Indicadores: Parciales (usuario proporciona 5 de 12)
8. Presupuesto: Total $50.000M, distribuido por programa

### Proceso (Skill)
1. Skill crea libro con 6 sheets
2. Sheet 1: Plan de Acción Integral con 48 filas (4 trimestres × 3 objetivos × 4 programas)
3. Sheet 2: Decreto 612 con 12 planes + estado + articulación
4. Sheet 3: Matriz de indicadores (12 indicadores)
5. Sheet 4: Articulación con PDD — Eje 1 de Bogotá Positiva
6. Sheet 5: Presupuesto por programa
7. Sheet 6: Glosario + referencias normativas

### Salida
- Archivo: `Plan_Accion_SecEducacion_Bogota_2026.xlsx`
- Tamaño: ~200KB
- Fórmulas: 48 en columna L + 48 en columna P + 48 en columna M (semáforo)
- Metadatos: SGDEA completos
- Instrucciones para actualización trimestral adjuntas

---

## Conexiones con otras skills

- **informe-gestion-entidad:** Usa datos del Plan de Acción para reportar avances
- **respuesta-pqrsdf-entidad:** Referencia objetivos/actividades relevantes en respuestas
- **oficio-memorando-entidad:** Cita el Plan de Acción en oficios de seguimiento o coordinación
- **cuenta-cobro:** Vincula presupuesto ejecutado con facturas de proveedores

---

## Notas técnicas finales

- **Tamaño máximo recomendado:** 1.000 filas (es decir, hasta ~200 proyectos/actividades)
- **Actualización:** Mínimo trimestral; máximo anual (pérdida de granularidad)
- **Validación:** Antes de publicar, revisar que no haya errores en fórmulas (verificar 5 filas muestrales)
- **Archivo versionado:** Guardar como `Plan_Accion_..._v01.xlsx`, `v02.xlsx`, etc.
  (cambios significativos → nueva versión)
- **SGDEA:** Registrar en tabla de retención documental con código de clasificación según
  Manual de Procedimientos de la entidad

---

## Conformidad MPIA-Bogotá — Acuerdo 003/2025 CDTD

### Sello de conformidad del documento

Incluir en el **pie de página** del documento generado:

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
Justificación del nivel: Asistencia en estructuración de planes de acción. Marco de planificación sin decisiones autónomas.
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
