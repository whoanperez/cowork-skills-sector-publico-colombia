---
name: manual-procedimientos-entidad
description: >
  Genera manuales de procedimientos y funciones en formato .docx para entidades del
  sector público colombiano. Estructura DAFP (Departamento Administrativo de la Función
  Pública): Objetivo, Alcance, Definiciones, Marco normativo, Generalidades, Procedimientos
  (con objetivo, alcance, responsable, actividades paso-a-paso, flujogramas, documentos,
  registros), Formatos y registros, Control de cambios. Alineado con NTC-ISO 9001:2015
  y NTCGP 1000:2009. Output: .docx profesional, tabla de contenidos, numeración,
  metadatos SGDEA, conformidad MPIA bajo riesgo.

  Usar SIEMPRE que alguien pida: manual de procedimientos, manual de funciones,
  documentación de procesos, procedimientos operativos, procesos paso a paso, manual
  de calidad, sistema de gestión de procesos, flujogramas operativos, procedimientos
  ISO, documentación de procesos DAFP, o cualquier variación que implique documentar
  procedimientos operativos de entidad colombiana.
---

# Skill: Manual de Procedimientos — Entidades Públicas Colombia

> Esta skill genera manuales de procedimientos en .docx, conforme a estructura DAFP,
> NTC-ISO 9001:2015 y NTCGP 1000:2009. Leer `references/normativa_comunicacion.md`
> para estructura recomendada, codificación de procesos y elementos de documentación.

---

## Paso 0 — Clasificación y recolección

### Preguntas obligatorias (en una sola interacción)

1. **Alcance del manual:**
   - [ ] Un proceso completo (ej: Proceso de Contratación)
   - [ ] Familia de procesos (ej: Procesos de Gestión Administrativa)
   - [ ] Manual integral de la entidad (todos los procesos)
   - Nombre del proceso(s) principal(es)

2. **Clasificación del proceso (Decreto 1083/2015):**
   - [ ] Estratégico (E) — Dirección y planificación (ej: Planeación, Dirección)
   - [ ] Misional (M) — Entrega de servicios (ej: Educación, Salud)
   - [ ] Apoyo (A) — Soporte a procesos (ej: Compras, RRHH)
   - [ ] Evaluación (V) — Control y auditoría (ej: Auditoría Interna)

3. **Codificación de procesos:**
   - ¿La entidad tiene mapa de procesos documentado?
   - ¿Sistema de codificación existente? (ej: GE-PR01, M-PR-02)
   - Si no: ¿Desea que la skill proponga codificación estándar?

4. **Estructura del procedimiento:**
   - Listado de procedimientos específicos (máximo 5 por manual)
   - Para CADA procedimiento:
     - Nombre exacto
     - Objetivo (máximo 1 párrafo)
     - Alcance (qué cubre, qué no)
     - Responsable principal (cargo/dependencia)
     - Documentos de entrada (inputs)
     - Documentos de salida (outputs)

5. **Actividades del proceso:**
   - Listado de pasos/actividades (secuencial)
   - Para cada actividad: descripción, responsable, documentos requeridos, tiempo estimado
   - ¿Existen variantes o excepciones? (ej: proceso normal vs proceso de urgencia)

6. **Flujograma:**
   - ¿Usuario tiene flujograma visualmente representado?
   - Si sí: subir imagen (.png, .pdf)
   - Si no: skill generará descripción textual de flujo (usuario valida)

7. **Marco normativo:**
   - Leyes, decretos, resoluciones que fundamentan el procedimiento
   - Políticas internas relacionadas
   - Normas de calidad aplicables (ISO, NTCGP)

8. **Plantilla institucional .docx:**
   - [ ] Sí, la entidad tiene template .docx (subir archivo)
   - [ ] No, usar formato estándar GTC-185

9. **Sistema de calidad:**
   - ¿La entidad tiene certificación ISO 9001:2015?
   - ¿Certificación NTCGP 1000:2009?
   - ¿Incluir criterios de medición y evaluación?

10. **Formatos y registros:**
    - Listado de formatos/plantillas asociadas al procedimiento
    - Ubicación de almacenamiento (carpeta, SharePoint, etc.)
    - Formularios que deben incluirse en el manual

### Preguntas opcionales

- ¿Incluir estudio de tiempos (tiempo estimado por actividad)?
- ¿Incluir matriz de riesgos operativos del procedimiento?
- ¿Incluir tabla de indicadores de desempeño del proceso?
- ¿Incluir glosario de términos técnicos específicos?
- ¿Incluir referencias cruzadas a otros procedimientos (relaciones)?

---

## Paso 1 — Estructura DAFP del manual

### Portada

```
[Logo entidad]
MANUAL DE PROCEDIMIENTOS
Nombre del proceso / Unidad administrativa

Versión: 01
Vigencia: Año
Última revisión: DD/MM/AAAA
Responsable: [Cargo/Dependencia]
```

### Tabla de contenidos (automática)

Generada en Word con estilos de encabezados.

### 1. Objetivo

**Propósito del manual (máximo 1 párrafo)**

Ej: "Establecer los procedimientos, responsabilidades y criterios que debe seguir la
Dirección de Compras para la gestión integral del proceso de contratación de bienes y
servicios, conforme a la Ley 80/1993 y normativa interna."

### 2. Alcance

**Qué cubre y qué no (máximo 1 párrafo)**

Ej: "Este manual aplica a todas las compras directas e indirectas realizadas por la
entidad, con excepción de las compras menores a 2 SMLV (aplican procedimiento expedito).
Cubre desde acto previo hasta cierre del contrato."

### 3. Definiciones / Glosario

**Términos técnicos y acrónimos relevantes (tabla)**

```
Término | Definición
--------|-----------------------------------------------------
ACT | Análisis de Conformidad Técnica — evaluación de cumplimiento
BPM | Business Process Management — modelado de procesos
CCP | Comité de Contratación Pública (si aplica)
...
```

### 4. Marco normativo

**Leyes, decretos, resoluciones aplicables (tabla)**

```
Norma | Año | Aspecto | Artículos relevantes
------|------|--------|----------------------
Ley 80 | 1993 | Contratación | Artículos 2, 25, 30
Decreto 1082 | 2015 | Régimen administrativo | Capítulo 1
...
```

### 5. Generalidades

**Políticas y lineamientos transversales aplicables a TODOS los procedimientos:**

- Responsabilidad institucional
- Lineamientos de confidencialidad y seguridad
- Criterios de atención al ciudadano
- Disposiciones sobre documentación
- Autoridades y delegaciones (si aplica)

### 6. Procedimientos [Sección principal]

Para CADA procedimiento (máximo 5 por manual), estructura:

```
6.1. [Nombre del Procedimiento]

6.1.1. Objetivo
       [Propósito específico]

6.1.2. Alcance
       [Límites del procedimiento]

6.1.3. Responsables y roles
       │
       ├─ Responsable principal: [Cargo]
       │   Responsabilidades: [Actividades clave]
       │
       ├─ Responsable de evaluación: [Cargo]
       │   Responsabilidades: [Qué evalúa]
       │
       └─ Responsable de registro: [Cargo]
           Responsabilidades: [Documentación]

6.1.4. Descripción de actividades

       ┌─────────────────────────────────────┐
       │ ACTIVIDAD 1: [Nombre]              │
       ├─────────────────────────────────────┤
       │ Responsable: [Cargo]               │
       │ Descripción: [Pasos detallados]    │
       │ Documentos entrada: [Listado]      │
       │ Documentos salida: [Listado]       │
       │ Tiempo estimado: [N minutos]       │
       │ Criterios de aceptación: [...]     │
       └─────────────────────────────────────┘

       ┌─────────────────────────────────────┐
       │ ACTIVIDAD 2: [Nombre]              │
       │ [idem]                             │
       └─────────────────────────────────────┘

6.1.5. Flujograma

       [Diagrama visual o descripción textual]

       Ej: Inicio → Actividad 1 → Decisión → Actividad 2a / Actividad 2b → Fin

6.1.6. Documentos de referencia

       │ Documento | Ubicación | Responsable |
       │-----------|-----------|-------------|
       │ Formato de solicitud | SharePoint | RRHH |

6.1.7. Registros y control

       │ Registro | Retención | Disposición |
       │----------|-----------|-------------|
       │ Log de solicitudes | 5 años | Destrucción controlada |

6.1.8. Indicadores de desempeño (opcional)

       │ Indicador | Fórmula | Meta | Periodicidad |
       │-----------|---------|------|-------------|
       │ % Cumplimiento tiempo | Trámites en plazo / Total | 90% | Mensual |

6.1.9. Anexo: Flujograma detallado [si es complejo]

```

### 7. Formatos y registros

**Listado de todos los formatos/plantillas usados en procedimientos**

```
┌─────────────────────────────────────────────────────────────┐
│ FORMATO 1: Solicitud de Compra                             │
├─────────────────────────────────────────────────────────────┤
│ Código: FORM-COMP-001                                      │
│ Vigencia: 2026                                             │
│ Responsable de actualización: Dirección de Compras         │
│ Ubicación de almacenamiento: S:\Formatos\Compras          │
│ Descripción: Formato para solicitud de bienes/servicios    │
│ [Incluir imagen del formato o PDF embebido]                │
└─────────────────────────────────────────────────────────────┘
```

### 8. Control de cambios

**Historial de versiones**

```
Versión | Fecha | Cambios | Aprobado por | Motivo
--------|-------|---------|--------------|-------
01 | DD/MM/AAAA | Documento inicial | [Director] | Implementación
02 | DD/MM/AAAA | Actualización de tiempos | [Director] | Mejora de eficiencia
...
```

---

## Paso 2 — Alineación con NTC-ISO 9001:2015 y NTCGP 1000:2009

### Elementos ISO 9001:2015 a incluir (si aplica)

- **Entradas del proceso:** Recursos requeridos
- **Salidas del proceso:** Resultados esperados
- **Responsabilidades:** Roles claros y autorizaciones
- **Procedimiento control:** Criterios de aceptación
- **Seguimiento y medición:** Indicadores del proceso
- **Cambios y mejora:** Anexo de control de cambios

### Elementos NTCGP 1000:2009 a incluir (si aplica)

- **Política y objetivos de calidad:** Referenciados en Generalidades
- **Documentación requerida:** Procedimientos, registros, formatos
- **Responsabilidades de dirección:** Roles organizacionales claros
- **Auditoría interna:** Criterios de seguimiento
- **Satisfacción del usuario:** Feedback en procedimientos de atención

### Mapeo a dimensiones MIPG (opcional)

Si procedimiento vinculado a objetivo estratégico:

```
Procedimiento: Gestión de Talento Humano
Dimensión MIPG: Talento Humano (Dimensión 1)
Política MIPG: Gestión del desempeño integral
```

---

## Paso 3 — Codificación de procesos

### Sistema de codificación recomendado

```
[TIPO_PROCESO] - [PROCEDIMIENTO] - [VERSIÓN]

Ej: E-PR-01 v02
    ├─ E = Estratégico
    ├─ PR = Procedimiento
    ├─ 01 = Primer procedimiento
    └─ v02 = Versión 2

Tipos:
├─ E = Estratégico
├─ M = Misional
├─ A = Apoyo
└─ V = Evaluación
```

### Si la entidad tiene codificación propia

Respetar sistema existente y validar en Paso 0.

### Codificación de formatos asociados

```
Formato: [CÓDIGO_PROCESO] - [TIPO_DOCUMENTO] - [CORRELATIVO]

Ej: E-PR-01-FT-001
    ├─ E-PR-01 = Procedimiento
    ├─ FT = Formato (otros: GU=Guía, IN=Instructivo, MN=Manual)
    └─ 001 = Primer formato
```

---

## Paso 4 — Especificaciones técnicas .docx

### Formato GTC-185

- **Tamaño:** Carta (21.59 × 27.94 cm)
- **Márgenes:** 3cm superior/izquierdo, 2.5cm inferior/derecho
- **Fuente cuerpo:** Arial o Times New Roman 11-12pt
- **Fuente tablas:** 10pt
- **Interlineado:** 1.5 líneas
- **Numeración:** Desde página 2 (con viñeta "Página X de Y")
- **Tabla de contenidos:** Obligatoria si >5 páginas

### Estilos y estructura

```
Encabezado 1 (Nivel 1): Negrita 14pt, espacio antes 12pt
├─ Encabezado 2 (Nivel 2): Negrita 12pt, espacio antes 10pt
│  └─ Encabezado 3 (Nivel 3): Negrita 11pt, espacio antes 8pt
│     └─ Párrafo normal: 11pt regular
│
Tablas:
├─ Encabezado tabla: Fondo gris claro (RGB 192,192,192), negrita
├─ Filas alternadas: Blanco y gris muy claro (RGB 242,242,242)
└─ Bordes: Simples, 0.5pt, color gris oscuro (RGB 128,128,128)
```

### Elementos obligatorios

- [ ] Portada con logo, título, versión, fecha
- [ ] Tabla de contenidos (automática)
- [ ] Encabezado: Nombre entidad
- [ ] Pie de página: Nombre entidad + versión + página
- [ ] Numeración de secciones (1, 2, 2.1, 2.1.1, etc.)
- [ ] Índice de tablas y figuras (si >3)

---

## Paso 5 — Flujogramas y diagramas

### Si usuario proporciona flujograma visual (.png, .pdf)

- Insertar como imagen embebida (no vinculada)
- Máximo ancho: 14cm (respeta márgenes)
- Incluir leyenda/referencia bajo imagen
- Altura mínima: 6cm (legible en impresión)

### Si NO hay flujograma visual

Skill genera descripción textual y sugiere forma visual:

```
Descripción textual:
"1. Inicio del proceso con Solicitud de Compra
2. Evaluación técnica (Responsable: Jefe Técnico)
   ├─ Si CUMPLE → Actividad 3
   └─ Si NO CUMPLE → Devolver a Solicitante (retorna a paso 1)
3. Evaluación presupuestal (Responsable: Hacienda)
   ├─ Si EXISTE PRESUPUESTO → Actividad 4
   └─ Si NO EXISTE → Rechazar
4. Publicación de proceso (Responsable: Compras)
5. Fin del proceso"

O Microsoft Visio / Lucidchart / SmartDraw diagram:
[Diagrama visual generado automáticamente]
```

---

## Paso 6 — Checklist de conformidad

### Conformidad DAFP, ISO 9001:2015, NTCGP 1000:2009

- [ ] Portada con logo, versión, fecha, responsable
- [ ] Tabla de contenidos automática
- [ ] Objetivo claro en máximo 1 párrafo (Sección 1)
- [ ] Alcance definido (Sección 2)
- [ ] Glosario de términos técnicos (Sección 3)
- [ ] Marco normativo con referencias completas (Sección 4)
- [ ] Generalidades con políticas transversales (Sección 5)
- [ ] Procedimientos con 9 subsecciones cada uno (Sección 6)
- [ ] Actividades con responsable, documentos, tiempo, criterios (6.X.4)
- [ ] Flujograma visual o textual (6.X.5)
- [ ] Documentos de referencia linkados/mencionados (6.X.6)
- [ ] Registros con retención documentaria (6.X.7)
- [ ] Indicadores de desempeño (opcional, 6.X.8)
- [ ] Formatos/registros con código de clasificación (Sección 7)
- [ ] Control de cambios con historial (Sección 8)
- [ ] Encabezados y pies de página consistentes
- [ ] Numeración continua y jerárquica
- [ ] Estilos de encabezado aplicados (genera tabla de contenidos)
- [ ] Tablas con bordes claros y encabezados diferenciados
- [ ] Máximo 50 líneas por página (evita mucho texto seguido)

### Validaciones de contenido

- [ ] No hay roles duplicados en matriz de responsabilidades
- [ ] Cada actividad tiene responsable claro (no "Equipo general")
- [ ] Criterios de aceptación/rechazo explícitos
- [ ] Tiempos estimados realistas (no menores a 5 minutos)
- [ ] Referencias normativas están vigentes (no leyes derogadas)
- [ ] Documentos de referencia existen y son accesibles

---

## Paso 7 — Metadatos para SGDEA

### Clasificación documental

```
Tipo documental: Manual de Procedimientos / Manual de Funciones
Serie: Documentación operativa
Subserie: [según TRD de la entidad] — Ej: Gestión Administrativa
Período: [Año de vigencia]
Fecha elaboración: [DD/MM/AAAA]
Soporte: Electrónico (Word .docx)
Vigencia: [2026] o [2026-2027]
Versión: [01, 02, etc.]
Responsable: [Nombre y cargo — usualmente jefe de proceso/dependencia]
Periodicidad revisión: [Anual/Bienal/Según cambios normativos]
Aceso: [Interno/Restringido/Público]

Procesos documentados: [Listado, ej: Contratación, RRHH, Compras]
Certificación calidad: [ISO 9001:2015 / NTCGP 1000:2009 / Ninguna]
Alineación MIPG: [Sí/No] — [Dimensiones si aplica]
```

---

## Paso 8 — Notas de uso y recomendaciones

### Distribución y capacitación

- **Versión controlada:** Distribuir como PDF para lectura (no editable)
- **Acceso:** Publicar en intranet institucional o carpeta compartida
- **Capacitación:** Realizar sesión de introducción con equipos operativos
- **Dudas:** Designar responsable de responder consultas sobre procedimientos

### Actualización y control de cambios

- **Revisión anual mínimo:** Validar vigencia de normativa y actividades
- **Cambios significativos:** Crear nueva versión (v01 → v02)
- **Cambios menores:** Anotar en Control de cambios sin cambiar versión
- **Trazabilidad:** Cada cambio con fecha, responsable, motivo

### Riesgos comunes

1. **Procedimiento genérico:** "Procesar solicitud" sin detalles.
   Solución: Desagregar en sub-actividades específicas (paso 1, 2, 3...).

2. **Responsable ambiguo:** "Área competente" sin nombre de cargo.
   Solución: Especificar cargo/dependencia exacta.

3. **Flujograma desactualizado:** Proceso cambia pero manual no se revisa.
   Solución: Establecer revisión trimestral con dueño del proceso.

4. **Normativa obsoleta:** Referencias a leyes derogadas.
   Solución: Validar vigencia en inicio de cada año fiscal.

5. **Formatos no embebidos:** "Véase el Formato X" pero no está incluido.
   Solución: Insertar imágenes o PDFs de formatos en Sección 7.

---

## Marco normativo embebido

Ver `references/normativa_comunicacion.md` para estructura DAFP y estándares de calidad.

**Normas principales:**

- **Decreto 1083/2015** — Régimen de Función Pública
  - Artículos sobre documentación de procesos y procedimientos

- **NTC-ISO 9001:2015** — Sistema de Gestión de Calidad
  - Requisitos de documentación de procesos
  - Identificación de entradas, salidas, responsables

- **NTCGP 1000:2009** — Norma Técnica de Calidad en la Gestión Pública
  - Documentación requerida por entidades públicas
  - Procedimientos, registros, formatos

- **Ley 594/2000** — Ley General de Archivos
  - Disposiciones sobre documentación y archivos
  - Tablas de retención documental

- **GTC-185** — Guía Técnica Colombiana para documentación sector público
  - Formato, márgenes, tipografía, estructura

- **Decreto 1499/2017** — MIPG
  - Alineación con dimensiones de gestión (si aplica)

---

## Conformidad MPIA-Bogotá — Acuerdo 003/2025 CDTD

### Nivel de riesgo: **BAJO**

**Justificación:** Documentación operativa de procesos internos. No genera decisiones
administrativas, no interactúa con ciudadanía, es soporte interno para standardización
operativa. Sin datos sensibles o decisorios.

### Sello de conformidad

Incluir en **pie de página** del documento generado:

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
AVISO DE USO DE IA — Acuerdo 003/2025 CDTD, Sección 10
Este manual fue elaborado con asistencia de inteligencia artificial
generativa. Su contenido requiere revisión, corrección y aprobación por
parte del servidor público responsable y de la dirección del proceso antes
de ser implementado como procedimiento oficial.
La IA no sustituye el conocimiento técnico del especialista del proceso.
El funcionario responsable asume la responsabilidad integral sobre el contenido final.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### Metadatos de trazabilidad IA

Incluir en metadatos SGDEA del documento:

```
--- Trazabilidad de uso de IA (Acuerdo 003/2025, Sección 10) ---
Herramienta utilizada: Skill manual-procedimientos-entidad
Tipo de apoyo recibido: Generación de manual de procedimientos
Categoría del sistema de IA: (g) Inteligencia Artificial Generativa
Nivel de riesgo MPIA: Bajo
Justificación: Documentación operativa interna, sin decisiones autónomas
Intervención humana requerida: Revisión técnica, corrección y aprobación
Fecha de generación: [DD/MM/AAAA]
Funcionario responsable: [Nombre y cargo del dueño del proceso]
```

### Checklist de conformidad MPIA-Bogotá (por documento)

- [ ] El manual es BORRADOR que requiere aprobación antes de implementación (Sección 10)
- [ ] Pie de página con aviso de IA incluido
- [ ] Metadatos de trazabilidad IA incluidos en metadatos SGDEA
- [ ] No se incluyeron datos personales sensibles, información clasificada o reservada
- [ ] El contenido NO sustituye el análisis técnico del especialista del proceso
- [ ] El contenido NO genera decisiones administrativas vinculantes
- [ ] El dueño del proceso ha revisado y valida antes de implementación oficial
- [ ] Manual será registrado en tabla de retención documental con código de serie

