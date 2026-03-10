---
name: oficio-memorando-entidad
description: >
  Crea oficios, memorandos y circulares institucionales para entidades del sector público colombiano.
  La skill adapta la plantilla de la entidad (si se sube), embebe la normativa del Archivo General
  de la Nación (Ley 594/2000, Acuerdo AGN 060/2001, GTC-185) y genera el documento en .docx listo
  para radicación en el SGDEA. Incluye checklist de conformidad normativa y modo completo con
  metadatos de radicación.

  Usar SIEMPRE que alguien pida: oficio, memorando, circular, comunicación oficial, carta
  institucional, respuesta a comunicación, solicitud formal, comunicación interna, comunicación
  externa, o cualquier documento de correspondencia oficial de una entidad pública colombiana.
  También activar cuando mencionen "elaborar comunicación", "redactar oficio", "responder
  radicado", "memo interno", "circular interna", o simplemente "necesito escribirle a [entidad]"
  en contexto de sector público.
---

# Skill: Oficio / Memorando / Circular — Entidades Públicas Colombia

> Esta skill produce documentos de correspondencia oficial para cualquier entidad del sector
> público colombiano, siguiendo el marco normativo del Archivo General de la Nación.
> Leer `references/normativa.md` para el detalle de cada norma antes de generar cualquier documento.

---

## Paso 0 — Recolección de información

Antes de generar el documento, preguntar al usuario lo siguiente (en una sola interacción):

### Preguntas obligatorias
1. **Tipo de documento**: ¿Oficio (externo), Memorando (interno) o Circular (múltiples destinatarios)?
2. **Entidad emisora**: nombre de la entidad, dependencia y cargo del firmante
3. **Destinatario**: nombre completo, cargo, entidad y ciudad
4. **Asunto**: descripción breve del tema (máximo 2 líneas)
5. **Contenido**: ¿qué debe decir el documento? (puede ser un resumen o instrucciones)

### Preguntas opcionales (si no se responden, usar valores por defecto)
- ¿Tiene referencia a un radicado previo? (si/no — cuál)
- ¿Hay anexos? (cuáles)
- ¿Va en copia a alguien? (quién)
- ¿Sube plantilla institucional? (archivo .docx — si no, usar formato estándar GTC-185)

### Detección automática de tipo especial
Si el destinatario es un **organismo de control** (Contraloría, Procuraduría, Defensoría, Personería,
Auditoría), activar modo `organismo_control = true` (ver sección de plazos normativos).

---

## Paso 1 — Adaptación de plantilla

Si el usuario sube un archivo `.docx` de plantilla institucional:
1. Extraer: fuentes, márgenes, encabezado/pie de página, colores, estructura del membrete
2. Aplicar esos estilos al documento generado
3. Indicar al usuario: "Adapté tu plantilla. Los campos de firma digital y código de radicado
   deben ser asignados por tu SGDEA (Orfeo, SIGA, Gestión Documental, etc.)"

Si **no** se sube plantilla: usar el formato técnico estándar (ver sección "Formato técnico base").

---

## Paso 2 — Generación del documento

### Estructura: Oficio (comunicación externa)

```
[MEMBRETE INSTITUCIONAL]
[Si hay plantilla: usar encabezado extraído. Si no: "[LOGO Y DATOS DE LA ENTIDAD]"]

Bogotá D.C., [DD de mes escrito de AAAA]
                                          Radicado N°: ________________
                                          [Para asignar en SGDEA]

Señor(a)
[NOMBRE COMPLETO DEL DESTINATARIO]
[Cargo]
[Entidad]
[Ciudad]

Asunto: [Máximo 2 líneas — sin punto final]

Referencia: [Radicado o norma de referencia — omitir si no aplica]

Respetado(a) señor(a) [Apellido]:

[Párrafo 1 — Contexto: quién escribe, desde qué entidad, con qué propósito]

[Párrafo 2 — Desarrollo: solicitud, respuesta, notificación o información específica]

[Párrafo 3 — Si organismo_control = true, incluir explícitamente:
  "De conformidad con [norma aplicable], la presente respuesta se remite dentro del
  término de [X] días hábiles contados a partir del [fecha de radicación del requerimiento]."
  Si no es organismo de control, usar cierre estándar: agradecimiento, expectativa, disponibilidad]

Atentamente,


[NOMBRE COMPLETO]
[Cargo]
[Dependencia]
[Entidad]
[Ciudad] | [Correo institucional] | [Teléfono]

Anexos: [Lista — omitir si no hay]
Copia: [Destinatarios — omitir si no hay]

Elaboró: [Nombre / Cargo]
Revisó: [Nombre / Cargo]
Aprobó: [Nombre / Cargo — si aplica]
```

### Estructura: Memorando (comunicación interna)

```
[MEMBRETE INSTITUCIONAL]

MEMORANDO

PARA:    [Nombre completo — Cargo — Dependencia]
DE:      [Nombre completo — Cargo — Dependencia]
ASUNTO:  [Descripción concisa]
FECHA:   [DD de mes escrito de AAAA]
RADICADO: ________________ [Para asignar en SGDEA]

[Párrafo 1 — Contexto o motivación]

[Párrafo 2 — Solicitud, instrucción o información específica. Si hay plazos, indicarlos.]

[Párrafo 3 — Cierre. Disponibilidad para aclaración.]

Atentamente,


[NOMBRE COMPLETO]
[Cargo] — [Dependencia]

Anexos: [Si aplica]
Copia: [Si aplica]

Elaboró: [Nombre / Cargo]
```

### Estructura: Circular

```
[MEMBRETE INSTITUCIONAL]

CIRCULAR N° [Número] DE [AAAA]

PARA:    [Grupo destinatario: "Todos los servidores públicos y contratistas" /
          "Directivos y Jefes de Dependencia" / especificar]
DE:      [Cargo y nombre del emisor]
ASUNTO:  [Descripción concisa]
FECHA:   [DD de mes escrito de AAAA]

[Párrafo 1 — Fundamento normativo o motivo de la circular]

[Párrafo 2 — Instrucción, lineamiento o información a comunicar]

[Párrafo 3 — Vigencia, obligatoriedad y punto de contacto para dudas]

Atentamente,


[NOMBRE COMPLETO]
[Cargo]
[Dependencia — Entidad]
```

---

## Paso 3 — Plazos normativos (modo completo)

Incluir siempre un bloque de "Alertas de Plazo" en el documento o como nota separada:

| Tipo de remitente         | Norma              | Plazo de respuesta          |
|---------------------------|--------------------|-----------------------------|
| Ciudadano / persona natural | Art. 14 CPACA (Ley 1437/2011) | **15 días hábiles** para peticiones generales |
| Queja o reclamo           | Art. 16 CPACA      | **15 días hábiles**         |
| Solicitud de documentos   | Art. 14 CPACA      | **10 días hábiles**         |
| Contraloría General       | Ley 42/1993, Art. 115 CGP | **5 días hábiles** (requerimientos de auditoría) |
| Procuraduría General      | Ley 734/2002 (CDU) | **5 días hábiles** (pliego de cargos), **10 días** (otros) |
| Defensoría del Pueblo     | Ley 24/1992        | **15 días hábiles**         |
| Personería Municipal      | Ley 136/1994       | **10 días hábiles**         |
| Congreso / Senado / Cámara | Art. 258 Ley 5/1992 | **5 días hábiles**         |
| Otro organismo de control | Norma específica   | **5 días hábiles** (criterio conservador) |

**Cálculo automático de fecha límite:**
- Si el usuario indica la **fecha de radicación**, calcular y mostrar:
  - Fecha límite de respuesta (en días hábiles, excluyendo sábados, domingos y festivos)
  - Días hábiles restantes desde hoy
  - Alerta si quedan **3 o menos días hábiles**

**Festivos nacionales 2026 (Colombia):**
1 ene, 12 ene, 23 mar, 2 abr, 3 abr, 1 may, 18 may, 8 jun, 29 jun, 20 jul, 7 ago, 17 ago,
12 oct, 2 nov, 16 nov, 8 dic, 25 dic.

---

## Paso 4 — Generación del archivo .docx

Usar la skill `docx` o python-docx para generar el archivo. Instrucciones técnicas:

```
Formato técnico base (si no hay plantilla del usuario):
- Tamaño página: Carta (21.59 × 27.94 cm)
- Márgenes: Superior 3cm, Inferior 3cm, Izquierdo 3cm, Derecho 2.5cm
- Fuente cuerpo: Arial o Times New Roman 12pt
- Fuente datos elaboración: 10pt
- Espaciado: sencillo (1.0), espacio entre párrafos: 6pt
- Alineación cuerpo: justificado
- Alineación membrete: centrado
- El campo "Radicado N°" debe dejarse en blanco con línea de subrayado
  para que el usuario lo complete en su SGDEA
```

Nombre del archivo: `[TipoDoc]_[AsuntoResumido]_[FechaAAAAMMDD].docx`
Ejemplo: `Oficio_SolicitudConvenio_20260309.docx`

---

## Paso 5 — Checklist de conformidad normativa (modo completo)

Presentar este checklist junto al archivo generado:

### Conformidad AGN — GTC-185 y Acuerdo 060/2001
- [ ] Membrete institucional o espacio reservado claramente identificado
- [ ] Fecha en formato completo (día en número, mes en letras, año en número)
- [ ] Número de radicado reservado para SGDEA (no inventado por la IA)
- [ ] Destinatario con: nombre completo, cargo, entidad y ciudad
- [ ] Asunto claro y conciso (máximo 2 líneas, sin punto final)
- [ ] Referencia indicada si es respuesta a comunicación previa
- [ ] Cuerpo no supera el límite: Oficio ≤ 2 páginas / Memorando ≤ 1 página / Circular ≤ 2 páginas
- [ ] Tratamiento formal y respetuoso ("usted" en todo el documento)
- [ ] Líneas de "Elaboró" y "Revisó" presentes
- [ ] Anexos listados correctamente (si aplica)
- [ ] Copia indicada (si aplica)
- [ ] Alerta de plazo de respuesta verificada (si es comunicación que requiere respuesta)
- [ ] Fuente y márgenes cumplen GTC-185 o plantilla institucional

### Metadatos sugeridos para radicación en SGDEA
```
Tipo documental: [Oficio / Memorando / Circular]
Serie documental: Correspondencia [Enviada / Interna / Circular]
Subserie: [según TRD de la entidad]
Fecha: [DD/MM/AAAA]
Folios: [número de páginas]
Soporte: Electrónico
Firmante: [Nombre y cargo]
Destinatario: [Nombre, entidad]
Asunto: [Texto del asunto]
```
> **Nota:** El código de serie/subserie y el radicado definitivo son asignados por el SGDEA
> de la entidad (Orfeo, SIGA, SEVEN, etc.). Esta skill no los genera.

---

## Marco normativo embebido

Ver `references/normativa.md` para el texto completo de referencia de cada norma.

**Normas principales:**
- **Ley 594/2000** — Ley General de Archivos: establece la obligatoriedad de gestión documental en entidades públicas
- **Acuerdo AGN 060/2001** — Pautas para la administración de comunicaciones oficiales (estructura, radicación, distribución)
- **GTC-185** — Norma técnica colombiana para elaboración de documentos comerciales y oficiales (márgenes, fuentes, estructura)
- **Ley 1437/2011 (CPACA)** — Código de Procedimiento Administrativo: plazos de respuesta a ciudadanos
- **Ley 734/2002 (CDU)** — Código Disciplinario Único: plazos ante organismos de control
- **Ley 42/1993** — Control fiscal: plazos ante Contraloría

---

## Notas de uso

- **Esta skill NO asigna radicados ni codifica series documentales.** Eso corresponde al SGDEA.
- **Esta skill NO aplica firma digital.** El documento generado es un borrador para revisión.
- El documento debe ser revisado por el servidor público responsable antes de radicación.
- Si la entidad tiene un Manual de Gestión Documental propio, sus reglas prevalecen sobre GTC-185.
- Para comunicaciones con organismos internacionales o embajadas, añadir protocolo diplomático.

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
Justificación del nivel: Asistencia en redacción de comunicaciones oficiales. Sin decisiones autónomas, sin datos sensibles por defecto, sin interacción directa con ciudadanía.
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
