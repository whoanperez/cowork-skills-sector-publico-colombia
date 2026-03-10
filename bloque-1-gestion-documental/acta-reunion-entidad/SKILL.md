---
name: acta-reunion-entidad
description: >
  Genera actas de reunión institucionales para entidades del sector público colombiano con
  estructura normativa GTC-185, tabla de compromisos con responsables y fechas, y control
  de asistencia. Produce .docx listo para firma y archivo en el SGDEA.

  Usar SIEMPRE que alguien pida: acta de reunión, acta de comité, acta de mesa de trabajo,
  acta de sesión, minuta de reunión, registro de reunión, "documenta esta reunión",
  "necesito el acta de", "acta del comité directivo", "acta de la mesa técnica",
  "acta de seguimiento", "levantar acta", o cualquier variación que implique documentar
  formalmente lo discutido y acordado en una reunión de una entidad pública colombiana.
  También activar cuando mencionen "compromisos de la reunión", "seguimiento a compromisos",
  o "tabla de compromisos".
---

# Skill: Acta de Reunión — Entidades Públicas Colombia

> Esta skill genera actas de reunión institucionales siguiendo la GTC-185 y las prácticas
> del sector público colombiano.
> Leer `references/normativa_actas.md` si se necesita el detalle normativo completo.

---

## Paso 0 — Recolección de información

### Preguntas obligatorias (en una sola interacción)

1. **¿Qué tipo de reunión fue?**
   - Comité (directivo, técnico, de seguimiento, etc.)
   - Mesa de trabajo
   - Reunión de seguimiento de proyecto
   - Sesión ordinaria / extraordinaria
   - Otro (especificar)

2. **Datos básicos:**
   - Entidad y dependencia que convoca
   - Lugar (físico o virtual — plataforma)
   - Fecha y hora de inicio / hora de finalización
   - Nombre del presidente o quien dirige la reunión
   - Nombre del secretario o relator (quien elabora el acta)

3. **Asistentes:**
   - Lista de asistentes (nombre, cargo, dependencia/entidad)
   - Invitados externos (si aplica)
   - Ausentes con excusa (si aplica)

4. **Orden del día / temas tratados:**
   - Lista de temas discutidos
   - Puede ser un resumen o notas sueltas — la skill los estructura

5. **Decisiones y compromisos:**
   - ¿Qué se decidió?
   - ¿Qué compromisos se adquirieron? (qué, quién, cuándo)

6. **¿Tiene plantilla institucional?** (archivo .docx)

### Información opcional
- Número de acta (si la entidad lleva consecutivo)
- Documentos presentados durante la reunión
- ¿Se requiere quórum? (sí/no — para comités con reglamento)
- Próxima reunión (fecha/hora si se definió)

---

## Paso 1 — Estructura del acta

```
[MEMBRETE INSTITUCIONAL]

ACTA N° [Número] DE [AAAA]

[NOMBRE DEL COMITÉ / REUNIÓN]

FECHA:          [DD de mes escrito de AAAA]
HORA:           [HH:MM] a [HH:MM]
LUGAR:          [Físico: dirección / Virtual: plataforma]
CONVOCA:        [Dependencia / Cargo]

═══════════════════════════════════════════════

ASISTENTES:

N° | Nombre completo          | Cargo              | Dependencia/Entidad
---|--------------------------|--------------------|-----------------------
1  | [Nombre]                 | [Cargo]            | [Dependencia]
2  | [Nombre]                 | [Cargo]            | [Dependencia]
...

INVITADOS:
[Lista si aplica]

AUSENTES CON EXCUSA:
[Lista si aplica]

VERIFICACIÓN DE QUÓRUM: [Si aplica: "Se verifica quórum con X de Y miembros"]

═══════════════════════════════════════════════

ORDEN DEL DÍA:

1. Verificación de quórum y apertura
2. Aprobación del acta anterior (Acta N° [anterior])
3. [Tema 1]
4. [Tema 2]
5. [Tema N]
6. Proposiciones y varios
7. Cierre y próxima reunión

═══════════════════════════════════════════════

DESARROLLO DE LA SESIÓN:

1. VERIFICACIÓN DE QUÓRUM Y APERTURA

[El/La presidente/a de la sesión, [Nombre], verifica quórum y da apertura
a la reunión a las [hora].]

2. APROBACIÓN DEL ACTA ANTERIOR

[Se somete a aprobación el Acta N° [anterior]. Resultado: Aprobada por
unanimidad / con observaciones.]

3. [TEMA 1 — TÍTULO]

[Desarrollo: quién presentó, qué se discutió, qué posiciones hubo,
qué se decidió. Redactar en tercera persona, pasado.]

[Continuar para cada tema del orden del día]

N. PROPOSICIONES Y VARIOS

[Temas adicionales planteados por los asistentes.]

N+1. CIERRE

[Se cierra la sesión a las [hora]. Se programa próxima reunión para
el [fecha] a las [hora] en [lugar].]

═══════════════════════════════════════════════

TABLA DE COMPROMISOS:

N° | Compromiso                    | Responsable        | Fecha límite  | Estado
---|-------------------------------|--------------------|---------------|--------
1  | [Descripción del compromiso]  | [Nombre — Cargo]   | [DD/MM/AAAA]  | Pendiente
2  | [Descripción]                 | [Nombre — Cargo]   | [DD/MM/AAAA]  | Pendiente
...

═══════════════════════════════════════════════

FIRMAS:

Para constancia se firma por quienes intervinieron:


______________________________          ______________________________
[Nombre completo]                       [Nombre completo]
[Cargo]                                 [Cargo]
Presidente de la sesión                 Secretario/Relator


______________________________          ______________________________
[Nombre completo]                       [Nombre completo]
[Cargo]                                 [Cargo]

Elaboró: [Nombre / Cargo]
Revisó: [Nombre / Cargo]
```

---

## Paso 2 — Reglas de redacción

### Tono y estilo
- Redactar en **tercera persona, tiempo pasado**: "El director presentó...", "Se acordó que..."
- Lenguaje **objetivo y neutro**: no interpretar, registrar lo que se dijo y decidió
- Si hubo desacuerdo, registrarlo sin tomar posición: "El funcionario X manifestó que...
  mientras que la funcionaria Y señaló que..."
- NO incluir opiniones personales del relator

### Compromisos
- Cada compromiso debe tener: **qué** se va a hacer, **quién** lo hace, **cuándo** debe estar listo
- Si no se definió fecha, indicar "Por definir" y alertar al usuario
- Si un compromiso viene de una reunión anterior y no se cumplió, marcarlo como "Pendiente (arrastre)"

### Quórum
- Si el usuario indica que es un comité con reglamento, verificar quórum:
  - Quórum deliberatorio: mayoría simple de miembros (50% + 1)
  - Quórum decisorio: depende del reglamento del comité
  - Si no hay quórum: "No se verificó quórum. La reunión se desarrolló como mesa de trabajo
    informativa. Las decisiones quedan sujetas a ratificación."

---

## Paso 3 — Adaptación de plantilla

- Si el usuario sube `.docx` de plantilla: extraer estilos y aplicar
- Si no: formato estándar GTC-185

```
Formato técnico base:
- Tamaño: Carta (21.59 × 27.94 cm)
- Márgenes: Superior 3cm, Inferior 3cm, Izquierdo 3cm, Derecho 2.5cm
- Fuente: Arial 12pt (cuerpo), Arial 10pt (tabla compromisos, datos elaboración)
- Tablas: bordes simples, encabezado en negrita, fondo gris claro en encabezado
- Espaciado: sencillo (1.0), 6pt entre párrafos
- Separadores: líneas horizontales entre secciones principales
```

Nombre del archivo: `Acta_[NombreComite]_[Numero]_[FechaAAAAMMDD].docx`
Ejemplo: `Acta_ComiteDirectivo_003_20260309.docx`

---

## Paso 4 — Checklist de conformidad

### Conformidad GTC-185 y gestión documental
- [ ] Membrete institucional o espacio reservado
- [ ] Número de acta consecutivo
- [ ] Fecha, hora de inicio y finalización
- [ ] Lugar (físico o virtual con plataforma)
- [ ] Lista de asistentes con nombre, cargo y dependencia
- [ ] Ausentes con excusa registrados
- [ ] Verificación de quórum (si aplica)
- [ ] Orden del día completo
- [ ] Desarrollo de cada punto del orden del día
- [ ] Decisiones registradas con claridad
- [ ] Tabla de compromisos con responsable y fecha
- [ ] Espacio para firmas de presidente y secretario
- [ ] Líneas de "Elaboró" y "Revisó"
- [ ] Redacción en tercera persona, tiempo pasado
- [ ] Tono objetivo sin interpretaciones

### Metadatos para SGDEA
```
Tipo documental: Acta
Serie: Actas de [nombre del comité/reunión]
Subserie: [según TRD de la entidad]
Fecha: [DD/MM/AAAA]
Folios: [número]
Soporte: Electrónico
Presidente sesión: [Nombre]
Secretario/Relator: [Nombre]
Asistentes: [N personas]
Compromisos: [N compromisos registrados]
```

---

## Notas de uso

- **Esta skill NO reemplaza el consecutivo de actas.** Si la entidad lleva numeración, el usuario
  debe indicar el número o la skill deja "[Número]" para completar.
- **Firmas:** El acta genera espacios para firma. Las firmas reales (manuscritas o digitales)
  son responsabilidad de los participantes.
- **Seguimiento:** La tabla de compromisos puede copiarse a una herramienta de seguimiento
  (Excel, plataforma de gestión). La skill no hace seguimiento automático.
- El acta debe circular entre los asistentes para revisión antes de ser firmada.

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
Justificación del nivel: Asistencia en estructuración de actas de reunión internas. Sin decisiones, sin datos sensibles, sin interacción ciudadana.
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
