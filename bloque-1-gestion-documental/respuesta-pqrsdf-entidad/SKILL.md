---
name: respuesta-pqrsdf-entidad
description: >
  Genera respuestas a Peticiones, Quejas, Reclamos, Sugerencias, Denuncias y Felicitaciones (PQRSDF)
  para entidades del sector público colombiano. Calcula automáticamente plazos legales según el tipo
  de peticionario (ciudadano, organismo de control, Congreso), alerta cuando quedan ≤3 días hábiles,
  y genera el documento .docx con checklist de conformidad normativa.

  Normativa embebida: CPACA (Ley 1437/2011), Ley 42/1993 (Contraloría), Ley 734/2002 (Procuraduría),
  Ley 5/1992 (Congreso), Ley 24/1992 (Defensoría), Ley 136/1994 (Personerías).

  Usar SIEMPRE que alguien pida: respuesta a derecho de petición, respuesta a PQRS, contestar
  requerimiento, responder queja, responder reclamo, atender petición, respuesta a tutela,
  contestar a la Contraloría, responder a la Procuraduría, responder a Personería, "me llegó un
  requerimiento", "tengo que contestar esto antes de", "cuántos días tengo para responder",
  "fecha límite de respuesta", o cualquier variación que implique responder una comunicación
  recibida con plazo legal en el sector público colombiano.
---

# Skill: Respuesta a PQRSDF — Entidades Públicas Colombia

> Esta skill genera respuestas a comunicaciones recibidas por entidades públicas colombianas,
> con cálculo automático de plazos legales y checklist de conformidad.
> Leer `references/normativa_pqrsdf.md` para el detalle completo de cada norma.

---

## Paso 0 — Clasificación y recolección de información

### Preguntas obligatorias (en una sola interacción)

1. **¿Qué tipo de comunicación recibió?**
   - Petición de interés general
   - Petición de interés particular
   - Petición de documentos / copias
   - Consulta
   - Queja
   - Reclamo
   - Sugerencia
   - Denuncia
   - Felicitación
   - Requerimiento de organismo de control
   - Requerimiento del Congreso
   - Acción de tutela

2. **¿Quién la envió?** (nombre, cargo, entidad o ciudadano, ciudad)

3. **¿Cuándo se radicó?** (fecha de radicado de entrada — esto determina el plazo)

4. **Entidad que responde**: nombre, dependencia y cargo del firmante

5. **¿Cuál es la respuesta?** (puede ser un resumen, instrucciones o puntos clave)

6. **¿Tiene plantilla institucional?** (archivo .docx — si no, usar formato GTC-185)

### Preguntas opcionales
- ¿Hay radicado de la comunicación original? (número)
- ¿Hay anexos en la respuesta? (cuáles)
- ¿Va en copia a alguien?
- ¿La petición estaba incompleta y se pidieron documentos adicionales? (Art. 15 CPACA — esto suspende el término)

---

## Paso 1 — Cálculo automático de plazos

Este es el corazón de la skill. Inmediatamente después de recibir el tipo de comunicación y la fecha de radicado, calcular y mostrar al usuario:

### Tabla de plazos según tipo

| Tipo de comunicación | Norma | Plazo |
|---|---|---|
| Petición de interés general | Art. 14 CPACA | **15 días hábiles** |
| Petición de interés particular | Art. 14 CPACA | **15 días hábiles** |
| Petición de documentos / copias | Art. 14 CPACA | **10 días hábiles** |
| Consulta | Art. 14 CPACA | **30 días hábiles** |
| Queja | Art. 16 CPACA | **15 días hábiles** |
| Reclamo | Art. 16 CPACA | **15 días hábiles** |
| Sugerencia | Art. 14 CPACA | **15 días hábiles** |
| Denuncia | Art. 14 CPACA | **15 días hábiles** |
| Requerimiento de Contraloría | Ley 42/1993, Art. 115 CGP | **5 días hábiles** (o el indicado en el requerimiento) |
| Requerimiento de Procuraduría | Ley 734/2002 | **5 días hábiles** (o el indicado) |
| Requerimiento de Defensoría | Ley 24/1992 | **15 días hábiles** |
| Requerimiento de Personería | Ley 136/1994 | **10 días hábiles** |
| Requerimiento del Congreso | Art. 258 Ley 5/1992 | **5 días hábiles** |
| Acción de tutela | Art. 86 Constitución | **10 días hábiles** (improrrogable) |

### Cálculo de fecha límite

Contar días hábiles desde el día siguiente a la radicación:
- Excluir sábados y domingos
- Excluir festivos nacionales

**Festivos Colombia 2026:**
1 ene, 12 ene, 23 mar, 2 abr, 3 abr, 1 may, 18 may, 8 jun, 15 jun, 29 jun, 20 jul, 7 ago, 17 ago,
12 oct, 2 nov, 16 nov, 8 dic, 25 dic.

### Presentación del cálculo al usuario

Mostrar SIEMPRE antes de generar el documento:

```
╔══════════════════════════════════════════════════╗
║  CÁLCULO DE PLAZO — [Tipo de comunicación]       ║
╠══════════════════════════════════════════════════╣
║  Fecha de radicado:     [DD/MM/AAAA]             ║
║  Plazo legal:           [X] días hábiles         ║
║  Norma aplicable:       [Ley/Artículo]           ║
║  Fecha límite:          [DD/MM/AAAA]             ║
║  Días hábiles restantes: [X] días                ║
║  Estado:                [🟢 A tiempo / 🟡 ≤3 días / 🔴 Vencido] ║
╚══════════════════════════════════════════════════╝
```

Si quedan **≤3 días hábiles**: alerta urgente.
Si está **vencido**: advertencia de que puede haber consecuencias disciplinarias (Art. 31 Ley 734/2002).

### Suspensión del término (Art. 15 CPACA)

Si el usuario indica que la petición estaba incompleta y se le pidieron documentos al peticionario:
- El término se suspende desde la fecha de requerimiento de documentos
- Se reanuda desde que el peticionario complete la solicitud
- Recalcular la fecha límite con el término restante

---

## Paso 2 — Generación del documento

### Estructura de la respuesta

```
[MEMBRETE INSTITUCIONAL]
[Si hay plantilla: usar encabezado extraído. Si no: "[LOGO Y DATOS DE LA ENTIDAD]"]

[Ciudad], [DD de mes escrito de AAAA]
                                          Radicado N°: ________________
                                          [Para asignar en SGDEA]

Señor(a)
[NOMBRE COMPLETO DEL PETICIONARIO]
[Cargo — si aplica]
[Entidad — si aplica]
[Dirección de notificación]
[Ciudad]

Asunto:  Respuesta a [tipo: petición / queja / reclamo / requerimiento]
         radicada bajo el N° [radicado de entrada]

Referencia: [Radicado de la comunicación original]

Respetado(a) señor(a) [Apellido]:

[Párrafo 1 — Acuse de recibo]
En atención a su [petición / queja / reclamo / requerimiento] radicada
el [fecha] bajo el N° [radicado], mediante la cual solicita [resumen
de lo solicitado], esta [dependencia] se permite dar respuesta en los
siguientes términos:

[Párrafo 2 — Fundamento normativo]
De conformidad con [norma aplicable: Art. 14 CPACA / Ley 42/1993 / etc.],
la entidad cuenta con un plazo de [X] días hábiles para dar respuesta.

[Párrafos 3-N — Desarrollo de la respuesta]
[Contenido sustantivo de la respuesta según las instrucciones del usuario]

[Párrafo final — Cierre y recursos]
- Si es petición ciudadana: informar los recursos de ley (reposición,
  apelación, queja) según Art. 74-80 CPACA.
- Si es organismo de control: indicar que se responde dentro del término
  legal y ofrecer información adicional si se requiere.
- Si es tutela: indicar que se acata la orden judicial / se contestan
  los hechos.

Lo anterior se expide dentro del término de [X] días hábiles contados
a partir del [fecha de radicación], en cumplimiento del [norma].

Atentamente,


[NOMBRE COMPLETO]
[Cargo]
[Dependencia]
[Entidad]

Anexos: [Lista — si aplica]
Copia: [Lista — si aplica]

Elaboró: [Nombre / Cargo]
Revisó: [Nombre / Cargo]
```

### Notas especiales por tipo

**Acción de tutela:**
- Plazo improrrogable de 10 días hábiles
- Incluir SIEMPRE: "La entidad se pronuncia sobre los hechos y pretensiones de la acción
  de tutela interpuesta por [nombre] ante [juzgado], radicada bajo el N° [radicado judicial]"
- La respuesta se dirige al Juzgado, con copia al accionante

**Silencio administrativo positivo (Art. 20 CPACA):**
- Si la respuesta está vencida, advertir al usuario:
  "⚠ ATENCIÓN: El plazo legal venció el [fecha]. Si aplica silencio administrativo positivo
  (Art. 20 CPACA), la petición podría entenderse resuelta favorablemente."

**Requerimiento de organismo de control con plazo específico:**
- Si el requerimiento de Contraloría/Procuraduría indica un plazo diferente al estándar,
  usar el plazo indicado en el requerimiento (prevalece sobre el genérico).

---

## Paso 3 — Adaptación de plantilla

Mismo mecanismo que la skill `oficio-memorando-entidad`:
- Si el usuario sube `.docx` de plantilla: extraer estilos y aplicar
- Si no: formato estándar GTC-185

```
Formato técnico base:
- Tamaño: Carta (21.59 × 27.94 cm)
- Márgenes: Superior 3cm, Inferior 3cm, Izquierdo 3cm, Derecho 2.5cm
- Fuente: Arial 12pt (cuerpo), 10pt (datos elaboración)
- Espaciado: sencillo (1.0), 6pt entre párrafos
- Alineación: justificado
```

Nombre del archivo: `Respuesta_[TipoPQRS]_[AsuntoResumido]_[FechaAAAAMMDD].docx`
Ejemplo: `Respuesta_Peticion_InformacionContratos_20260309.docx`

---

## Paso 4 — Checklist de conformidad normativa

### Conformidad CPACA y normativa aplicable
- [ ] Tipo de PQRSDF correctamente clasificado
- [ ] Plazo legal correctamente identificado y calculado
- [ ] Respuesta dentro del término legal (si no, advertencia de silencio administrativo)
- [ ] Acuse de recibo con número de radicado de la petición original
- [ ] Fundamento normativo citado en el cuerpo de la respuesta
- [ ] Contenido sustantivo que responde efectivamente lo solicitado (no evasivo)
- [ ] Recursos de ley informados al peticionario (si aplica)
- [ ] Fecha en formato completo
- [ ] Radicado de salida reservado para SGDEA
- [ ] Destinatario con datos completos
- [ ] Líneas de "Elaboró" y "Revisó"
- [ ] Fuente y márgenes GTC-185 o plantilla institucional

### Alerta de plazo
```
Tipo:               [PQRS clasificado]
Radicado entrada:   [Número]
Fecha radicado:     [DD/MM/AAAA]
Plazo legal:        [X] días hábiles — [Norma]
Fecha límite:       [DD/MM/AAAA]
Días restantes:     [X] días hábiles
Estado:             [A tiempo / Próximo a vencer / VENCIDO]
```

### Metadatos para SGDEA
```
Tipo documental: Respuesta a [PQRSDF]
Serie: Correspondencia Enviada
Subserie: [según TRD de la entidad]
Radicado asociado: [radicado de entrada]
Fecha: [DD/MM/AAAA]
Folios: [número]
Soporte: Electrónico
Firmante: [Nombre y cargo]
Destinatario: [Nombre]
Asunto: Respuesta a [tipo] radicado N° [número]
```

---

## Marco normativo embebido

Ver `references/normativa_pqrsdf.md` para artículos completos.

**Normas principales:**
- **Ley 1437/2011 (CPACA)** — Arts. 13-33: derecho de petición, plazos, silencio administrativo
- **Ley 1755/2015** — Regulación del derecho de petición (reforma parcial CPACA)
- **Ley 42/1993** — Requerimientos de Contraloría
- **Ley 734/2002** — Requerimientos de Procuraduría, consecuencias disciplinarias por no responder
- **Ley 5/1992** — Requerimientos del Congreso
- **Constitución Política** — Art. 23 (derecho de petición), Art. 86 (tutela)
- **GTC-185** — Formato del documento

---

## Notas de uso

- **Esta skill NO asigna radicados.** El radicado de salida lo asigna el SGDEA.
- **Esta skill NO determina si hay silencio administrativo positivo.** Solo advierte si el plazo venció.
- **Tutelas:** La respuesta es un insumo para el apoderado/oficina jurídica. No reemplaza concepto jurídico.
- El usuario siempre debe revisar el contenido sustantivo antes de radicar.
- Para actualizar festivos de años futuros, consultar el decreto del Ministerio del Interior.

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
Nivel de riesgo MPIA: Medio
Justificación del nivel: Genera borradores de respuestas a peticiones ciudadanas con cálculo de plazos legales. Interacción indirecta con ciudadanía. Riesgo de error en plazos.
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
