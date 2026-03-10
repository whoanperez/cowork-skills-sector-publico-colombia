---
name: carta-compromiso-entidad
description: >
  Genera cartas de compromiso y memorandos de entendimiento (MOU) en formato .docx
  para entidades del sector público colombiano. Tipos: Carta de Intención, Memorando
  de Entendimiento (MOU), Acuerdo Marco de Cooperación, Declaración Conjunta. Estructura:
  Identificación de partes, Antecedentes, Objeto, Compromisos de cada parte, Plazo,
  Seguimiento, Propiedad intelectual, Cláusula NO obligaciones financieras, Firmas.
  Conforme a Ley 489/1998 Art. 95-96 (convenios interadministrativos). IMPORTANTE:
  Genera advertencia si documento crea obligaciones patrimoniales (redirige a contrato
  formal). Output: .docx profesional, metadatos SGDEA, conformidad MPIA bajo riesgo.

  Usar SIEMPRE que alguien pida: memorando de entendimiento, MOU, carta de compromiso,
  carta de intención, acuerdo marco de cooperación, acuerdo interadministrativo,
  declaración conjunta, carta de intención cooperación, MOU entre entidades, convenio
  de cooperación, o cualquier variación que implique crear documento de voluntad de
  cooperación (no vinculante patrimonialmente) entre entidades públicas o aliados.
---

# Skill: Carta de Compromiso / Memorando de Entendimiento — Entidades Públicas Colombia

> Esta skill genera cartas de compromiso y MOUs en .docx, conforme a Ley 489/1998
> Art. 95-96 (convenios interadministrativos). ADVERTENCIA: Si el documento genera
> obligaciones financieras o patrimoniales, NO es un MOU sino un CONTRATO que requiere
> proceso formal de contratación. Leer `references/normativa_comunicacion.md` para
> naturaleza jurídica, elementos obligatorios y limitaciones.

---

## Paso 0 — Clasificación y recolección

### Preguntas obligatorias (en una sola interacción)

1. **Tipo de documento:**
   - [ ] Carta de Intención (voluntad inicial, no vinculante)
   - [ ] Memorando de Entendimiento (MOU) — colaboración de mediano plazo
   - [ ] Acuerdo Marco de Cooperación (AMC) — más formal que MOU
   - [ ] Declaración Conjunta — posición común sobre tema específico
   - [ ] Otro (especificar)

   **ADVERTENCIA:** Si va a incluir obligaciones FINANCIERAS (dinero, bienes, servicios
   pagados), esto NO es un MOU sino un CONTRATO. Contactar con Jurídica/Procuraduría
   para iniciar proceso formal de contratación (Ley 80/1993, Decreto 1082/2015).

2. **Partes del documento:**
   - Entidad firmante 1:
     * Nombre legal exacto
     * Tipo (Ministerio, Instituto, Gobernación, Municipio, Empresa, ONG, etc.)
     * Representante legal (nombre, cargo, cédula)
     * Correo oficial
   - Entidad firmante 2:
     * [Idem para segunda entidad]
   - ¿Hay terceras partes? (si sí: repetar datos para cada una)

3. **Antecedentes y contexto:**
   - Relación anterior entre partes (si existe)
   - Contexto político/institucional que motiva el MOU (máximo 2 párrafos)
   - Vacío o necesidad que se quiere llenar

4. **Objeto del memorando:**
   - Propósito general (máximo 1 párrafo)
   - Áreas específicas de cooperación (máximo 5 líneas):
     * Ej: Capacitación, investigación conjunta, intercambio de información, coordinación
       en procesos administrativos, apoyo en eventos, etc.

5. **Compromisos de cada parte:**
   - Para CADA parte, listado de compromisos específicos (máximo 5 por parte):
     * Formato: "Acción / Responsable / Periodicidad / Documentación de evidencia"
     * Ej: "Proporcionar acceso a base de datos de licencias / Dirección de Tecnología / Permanente / Reporte mensual"
   - IMPORTANTE: Verificar que NO son obligaciones de **dar dinero** (eso sería contrato)

6. **Plazo de vigencia:**
   - Fecha de inicio (cuando entra en vigor)
   - Duración (ej: 1 año, 2 años, indefinido, hasta cierta fecha)
   - ¿Renovación automática o requiere firma nueva?
   - ¿Cláusula de terminación anticipada?

7. **Seguimiento y evaluación:**
   - ¿Hay comité de seguimiento?
   - Periodicidad de reuniones (trimestral, semestral, anual)
   - ¿Quiénes integran el comité? (nombres/cargos)
   - Indicadores de cumplimiento (si aplica)

8. **Propiedad intelectual:**
   - ¿Voy a generar productos/IP conjunta?
   - Si sí: ¿Quién es propietario de la IP?
   - ¿Cómo se cita/reconoce contribución de cada parte?

9. **Plantilla institucional .docx:**
   - [ ] Sí, la entidad tiene template .docx (subir archivo)
   - [ ] No, usar formato estándar GTC-185

10. **Normas aplicables (además de Ley 489):**
    - ¿Hay otras leyes/decretos que apliquen? (ej: normativa ambiental, de educación)
    - ¿Políticas internas de la entidad sobre MOUs?

### Preguntas opcionales

- ¿Incluir anexo con documentos de identidad de representantes?
- ¿Incluir anexo con descripción detallada de compromisos (matriz RACI)?
- ¿Incluir cláusula de confidencialidad?
- ¿Incluir mecanismo de solución de controversias (mediación, arbitraje)?
- ¿Lenguaje en español únicamente o bilíngue (inglés)?

---

## Paso 1 — Estructura según tipo de documento

### Estructura base para todos los tipos (secuencia obligatoria)

```
1. Portada
   ├─ Logos de entidades
   ├─ Tipo de documento (MEMORANDO DE ENTENDIMIENTO / CARTA DE INTENCIÓN)
   └─ Fecha de firma

2. Encabezado
   ├─ Referencia: MOU-[AÑO]-[CORRELATIVO]
   │  (Ej: MOU-2026-001)
   └─ Lugar y fecha de firma

3. Identificación de las partes
   ├─ Entidad 1: [Nombre legal], con [representante]
   │  Cargo: [Cargo], Cédula: [Número]
   │
   ├─ Entidad 2: [Nombre legal], con [representante]
   │  Cargo: [Cargo], Cédula: [Número]
   │
   └─ [Si hay más partes: ídem]

4. CONSIDERANDOS (Antecedentes y consideraciones)
   ├─ Que [Hechos iniciales que motivan]
   ├─ Que [Contexto institucional]
   ├─ Que [Beneficios mutuos]
   └─ Que [Deseo de cooperación]

5. ACUERDAN (Objeto y cuerpo principal)

6. Mecanismo de seguimiento

7. Vigencia

8. Disposiciones finales

9. FIRMAN

10. [Anexos si aplica]
```

---

## Paso 2 — Desarrollo sección por sección

### 1. Portada (opcional pero recomendada)

```
                          [LOGO ENTIDAD 1]  [LOGO ENTIDAD 2]

                    MEMORANDO DE ENTENDIMIENTO
                    (u otro tipo de documento)

              Sobre cooperación en [TEMA GENERAL]

                   Entre [Nombre Entidad 1]
                         y
                     [Nombre Entidad 2]

                  Celebrado en [Lugar], en la ciudad de [Ciudad]
                            el [Día] de [Mes] de [Año]
```

### 2. Encabezado y datos administrativos

```
MEMORANDO DE ENTENDIMIENTO

Referencia: MOU-2026-001
Lugar de celebración: Bogotá, D.C.
Fecha de celebración: 10 de marzo de 2026
Vigencia: 2 años a partir de la fecha
Responsable institucional: [Nombre y cargo]
```

### 3. Identificación de las partes

```
IDENTIFICACIÓN DE LAS PARTES

En la ciudad de [Ciudad], siendo las [Hora], del día [Día] de [Mes]
de [Año], se reúnen:

PRIMERA PARTE:

    Denominación: [Nombre legal exacto de Entidad 1]
    NIT/RUC: [Número]
    Naturaleza jurídica: [Entidad territorial/Nacional/Instituto/ONG]
    Representante legal: [Nombre completo]
    Cargo: [Cargo exacto]
    Cédula de ciudadanía: [Número y expedida en]
    Domicilio: [Dirección completa]
    Correo electrónico: [Correo oficial]
    Teléfono: [Número oficial]

SEGUNDA PARTE:

    [Idem para entidad 2]

En adelante, las partes se referirán indistintamente como "LA PRIMERA PARTE"
y "LA SEGUNDA PARTE", o "LAS PARTES" cuando se refieran a ambas.
```

### 4. Considerandos

**Estilo legal pero accesible:**

```
CONSIDERANDOS

Que LA PRIMERA PARTE, en ejercicio de sus funciones de [Función institucional],
tiene la responsabilidad de [Misión general];

Que LA SEGUNDA PARTE, en su calidad de [Tipo de entidad], trabaja en los campos
de [Área de actuación];

Que ambas partes reconocen la importancia de [Área de interés común] y consideran
que la cooperación mutua puede contribuir a [Beneficio general];

Que las partes desean establecer un marco de cooperación que permita [Objetivo común]
sin crear obligaciones patrimoniales entre ellas;

Que esta cooperación se alinea con [Marco normativo / Plan de Desarrollo / Decreto];

En virtud de lo anterior, LAS PARTES ACUERDAN:
```

### 5. ACUERDAN — Cuerpo principal

```
ARTÍCULO 1. OBJETO

El presente Memorando de Entendimiento tiene por objeto establecer un marco de
cooperación entre LAS PARTES para [Descripción general del propósito].

Esta cooperación NO genera obligaciones financieras o patrimoniales entre las partes,
y se fundamenta en el principio de voluntariedad y beneficio mutuo.

─────────────────────────────────────────────────────────────────────────────

ARTÍCULO 2. ÁREAS DE COOPERACIÓN

Las partes acuerdan cooperar en las siguientes áreas específicas:

2.1. [Área 1: descripción específica]
2.2. [Área 2: descripción específica]
2.3. [Área 3: descripción específica]
[máximo 5 áreas]

─────────────────────────────────────────────────────────────────────────────

ARTÍCULO 3. COMPROMISOS DE LA PRIMERA PARTE

LA PRIMERA PARTE se compromete a:

3.1. [Acción específica], responsabilidad del [Cargo], con periodicidad [Frecuencia]
     Evidencia de cumplimiento: [Qué se entrega/cómo se verifica]

3.2. [Acción específica], responsabilidad del [Cargo], con periodicidad [Frecuencia]
     Evidencia de cumplimiento: [Qué se entrega/cómo se verifica]

[máximo 5 compromisos]

NOTA IMPORTANTE: Estos compromisos se cumplen con RECURSOS PRESUPUESTARIOS PROPIOS
de LA PRIMERA PARTE, sin transferencia de fondos a LA SEGUNDA PARTE.

─────────────────────────────────────────────────────────────────────────────

ARTÍCULO 4. COMPROMISOS DE LA SEGUNDA PARTE

LA SEGUNDA PARTE se compromete a:

[Estructura idéntica a Artículo 3]

─────────────────────────────────────────────────────────────────────────────

ARTÍCULO 5. NO CREACIÓN DE OBLIGACIONES FINANCIERAS

Ambas partes reconocen y acuerdan explícitamente que:

5.1. Este Memorando NO constituye un contrato de compraventa, suministro o servicios.
5.2. NO genera obligación de pago de dinero entre las partes.
5.3. NO crea deuda patrimonial.
5.4. Los compromisos se cumplen con recursos presupuestarios propios.
5.5. Si durante la ejecución surgiera necesidad de transferencia de recursos,
    las partes deberán celebrar CONTRATO FORMAL conforme a Ley 80/1993 y
    Decreto 1082/2015, con tramitación de procesos de contratación pública.
```

### 6. Mecanismo de seguimiento y coordinación

```
─────────────────────────────────────────────────────────────────────────────

ARTÍCULO 6. COMITÉ DE SEGUIMIENTO

Para asegurar el cumplimiento de los compromisos, las partes acuerdan crear
un COMITÉ DE SEGUIMIENTO integrado por:

POR LA PRIMERA PARTE:
├─ [Cargo 1], como coordinador principal
└─ [Cargo 2], como suplente

POR LA SEGUNDA PARTE:
├─ [Cargo 1], como coordinador principal
└─ [Cargo 2], como suplente

El Comité se reunirá [mensual/trimestral/semestral/anual] para:
├─ Revisar estado de cumplimiento de compromisos
├─ Identificar obstáculos
├─ Ajustar cronogramas si es necesario
└─ Documentar avances en acta

Responsable de convocar: [Cargo de la primera parte]
Lugar de reunión: [Alternadamente en sedes de las partes / Presencialmente / Virtual]

─────────────────────────────────────────────────────────────────────────────

ARTÍCULO 7. REPORTES Y DOCUMENTACIÓN

Las partes se comprometen a documentar el cumplimiento mediante:

7.1. Reporte [Trimestral/Semestral/Anual] de LA PRIMERA PARTE, enviado a [Contacto]
7.2. Reporte [Trimestral/Semestral/Anual] de LA SEGUNDA PARTE, enviado a [Contacto]
7.3. Actas de Comité de Seguimiento (una copia a cada parte)
7.4. Registro de [Documentos/Datos/Evidencias] de cooperación

Responsable de consolidación: [Cargo coordinador principal]
```

### 7. Vigencia

```
─────────────────────────────────────────────────────────────────────────────

ARTÍCULO 8. VIGENCIA Y TERMINACIÓN

8.1. ENTRADA EN VIGOR
    Este Memorando entra en vigor a partir de la fecha de su firma
    por ambas partes (hoy [Día] de [Mes] de [Año]).

8.2. DURACIÓN
    La vigencia de este Memorando es de [X años / X meses / Indefinida],
    contados a partir de la entrada en vigor.

8.3. RENOVACIÓN
    [ ] A. Renovación automática por períodos iguales, salvo denuncia
       escrita con 30 días de anticipación a su vencimiento.

    [ ] B. Requiere firma nueva de ambas partes para continuar.

8.4. TERMINACIÓN ANTICIPADA
    Cualquiera de las partes podrá terminar este Memorando con:
    ├─ Notificación escrita con [30/60/90] días de anticipación
    ├─ Causales: Imposibilidad legal, cambio normativo, interés público
    └─ Los compromisos en ejecución se cumplen hasta la fecha de terminación
```

### 8. Disposiciones finales

```
─────────────────────────────────────────────────────────────────────────────

ARTÍCULO 9. CONFIDENCIALIDAD

[ ] Si se requiere:
Las partes acuerdan que la información compartida bajo este Memorando será
tratada conforme a [Ley 1581/2012 (LSCA), Ley 1712/2014 (Transparencia), Decreto 1377/2013].
Información clasificada será marcada como "RESERVADA" y manejada según normativa.

─────────────────────────────────────────────────────────────────────────────

ARTÍCULO 10. PROPIEDAD INTELECTUAL

[ ] Si se generan productos conjuntos:

10.1. AUTORÍA COMPARTIDA
     Los productos desarrollados bajo este Memorando serán considerados de
     autoría compartida entre LAS PARTES.

10.2. USO Y DIFUSIÓN
     Ambas partes tienen derecho a usar y citar los productos resultantes,
     con reconocimiento de la contribución de ambas partes.

10.3. PUBLICACIÓN
     Cualquier publicación requiere consentimiento previo de ambas partes
     y mención explícita de ambas como autores/co-autores.

─────────────────────────────────────────────────────────────────────────────

ARTÍCULO 11. SOLUCIÓN DE CONTROVERSIAS

En caso de desacuerdo sobre la interpretación de este Memorando:

11.1. DIÁLOGO INICIAL
      Las partes buscarán resolución a través de diálogo directo entre
      coordinadores de cada parte (máximo 15 días).

11.2. ESCALAMIENTO
      Si no hay resolución, se eleva a directores/jefes respectivos (máximo 30 días).

11.3. MEDIACIÓN
      Si persiste el desacuerdo, ambas partes convocarán mediador neutral
      (designado de común acuerdo).

[ ] 11.4. ARBITRAJE (si aplica): En caso de persistir controversia,
      se somete a [Cámara de Comercio/Centro de Arbitraje] para procedimiento
      arbitral conforme a [Ley 1563/2012].

─────────────────────────────────────────────────────────────────────────────

ARTÍCULO 12. ENMIENDAS Y MODIFICACIONES

Este Memorando solo podrá ser modificado mediante acuerdo escrito firmado
por ambas partes, que se anexará como "Enmienda No. [X]" con fecha.

─────────────────────────────────────────────────────────────────────────────

ARTÍCULO 13. NORMATIVA APLICABLE

Este Memorando se rige por:
├─ Ley 489/1998 (Artículos 95-96, Convenios interadministrativos)
├─ Ley 594/2000 (Gestión documental)
├─ Ley 1712/2014 (Transparencia y acceso a información)
├─ Decreto 767/2022 (Política de Gobierno Digital)
└─ [Otras normas aplicables según naturaleza de cooperación]

─────────────────────────────────────────────────────────────────────────────

ARTÍCULO 14. EFECTOS Y LIMITACIONES

14.1. Este Memorando expresa VOLUNTAD DE COOPERACIÓN, no es contrato vinculante.
14.2. LAS PARTES actúan con autonomía institucional en el cumplimiento
      de sus compromisos.
14.3. Incumplimiento de compromisos es responsabilidad de la parte,
      pero NO genera demanda legal (es asunto administrativo/reputacional).
14.4. Si se requiere generar obligaciones contractuales, se debe firmar
      CONTRATO FORMAL con procesos de contratación pública.
```

### 9. Firmas y suscripción

```
─────────────────────────────────────────────────────────────────────────────

FIRMAN

En constancia de lo anterior, las partes firman el presente Memorando de Entendimiento
en la ciudad de [Bogotá], el día [Día] de [Mes] de [Año], en dos ejemplares originales,
de igual tenor y validez.

POR LA PRIMERA PARTE:

[Línea para firma]
_________________________________
[Nombre completo del representante]
Cargo: [Cargo exacto]
Cédula: [Número]
Fecha: [DD/MM/AAAA]


POR LA SEGUNDA PARTE:

[Línea para firma]
_________________________________
[Nombre completo del representante]
Cargo: [Cargo exacto]
Cédula: [Número]
Fecha: [DD/MM/AAAA]

─────────────────────────────────────────────────────────────────────────────

VISTO BUENO / APROBACIÓN JURÍDICA (Interno)

[Opcional: Firma de Asesoría Jurídica de cada entidad]

Asesor jurídico [Entidad 1]:
_________________________________
Nombre y Cargo

Asesor jurídico [Entidad 2]:
_________________________________
Nombre y Cargo

Date: [DD/MM/AAAA]
```

### 10. Anexos (opcionales)

```
ANEXO 1: Descripción detallada de compromisos
[Matriz RACI con Responsable, Accountable, Consulted, Informed]

ANEXO 2: Indicadores de cumplimiento (si aplica)
[Tabla de métricas de desempeño]

ANEXO 3: Cronograma de actividades
[Calendario de hitos y entregas]

ANEXO 4: Documentos de identidad de representantes
[Copias de cédula/documento de identificación]

ANEXO 5: Referencias normativas
[Listado de decretos, leyes, resoluciones aplicables]
```

---

## Paso 3 — Advertencia sobre obligaciones patrimoniales

### VALIDACIÓN CRÍTICA (Skill debe preguntar si...)

Si el usuario menciona:
- "Transferencia de fondos entre partes"
- "Pago de servicios o suministros"
- "Donación de bienes"
- "Prestación de servicios remunerada"
- "Presupuesto compartido"
- "Tarifa o canon"
- Cualquier mención de DINERO

**SKILL GENERA ADVERTENCIA:**

```
⚠️  ADVERTENCIA CRÍTICA ⚠️

El documento que está intentando crear contiene OBLIGACIONES FINANCIERAS O PATRIMONIALES.

Un Memorando de Entendimiento NO puede crear estas obligaciones.
Si las partes necesitan transferir dinero o bienes, deben celebrar CONTRATO FORMAL.

PASO REQUERIDO:
├─ Contactar con Dirección Jurídica / Procuraduría de su entidad
├─ Iniciar proceso de contratación pública conforme a:
│  ├─ Ley 80/1993 (Estatuto de Contratación Pública)
│  └─ Decreto 1082/2015 (Régimen de Contratación)
└─ Generar documentos: Especificaciones técnicas, presupuestos, pliegos

ALTERNATIVA:
Si desea crear SOLO documento de intención sin obligaciones financieras,
redefina los compromisos como acciones SIN intercambio de dinero.

¿Desea:
[ ] A. Redefinir compromisos para eliminar obligaciones financieras
[ ] B. Suspender este documento y contactar con Jurídica para CONTRATO
```

---

## Paso 4 — Especificaciones técnicas .docx

### Formato GTC-185

- **Tamaño:** Carta (21.59 × 27.94 cm)
- **Márgenes:** 3cm superior/izquierdo, 2.5cm inferior/derecho
- **Fuente cuerpo:** Arial o Times New Roman 11-12pt
- **Interlineado:** 1.5 líneas (facilita lectura y firma manuscrita)
- **Numeración:** Desde página 2 ("Página X de Y")
- **Espacio entre párrafos:** 6pt antes, 6pt después

### Estilos

```
Título (Portada): 18pt negrita, centrado
Encabezado (CONSIDERANDOS, FIRMAN): 12pt negrita, izquierdo
Artículos (ARTÍCULO 1): 11pt negrita
Numeración interna (1.1, 1.2): 11pt regular
Párrafos: 11pt regular

CONSIDERANDOS: Iniciar con "Que" y punto.
Cuerpo: Párrafos de máximo 5 líneas (legibilidad para firma).
```

### Elementos obligatorios

- [ ] Logos de ambas entidades en portada
- [ ] Referencia única (MOU-AÑO-CORRELATIVO)
- [ ] Lugar y fecha de firma
- [ ] Identificación completa de representantes (nombres, cargos, cédulas)
- [ ] Considerandos (mínimo 3)
- [ ] Artículos numerados (mínimo 8)
- [ ] Espacios para firma de ambas partes (dactilares + nombre)
- [ ] Espacios para sello/visto bueno jurídico (si aplica)
- [ ] Fecha de firma

---

## Paso 5 — Tipos específicos de documento

### Carta de Intención (menos formal)

```
Estructura reducida:
├─ Encabezado con logos
├─ Destinatario: [Entidad / Persona]
├─ Asunto: Intención de cooperación en [Tema]
├─ Cuerpo (máximo 4 párrafos):
│  ├─ Párr. 1: Presentación de la entidad y propósito general
│  ├─ Párr. 2: Áreas de interés común
│  ├─ Párr. 3: Beneficios esperados
│  └─ Párr. 4: Invitación a iniciar diálogos formales
├─ Cierre: "Atentamente" / "Respetuosamente"
└─ Firma de representante legal

Duración: 1-2 páginas
Vinculación legal: Mínima (es expresión de interés)
```

### Memorando de Entendimiento (MOU) — ESTRUCTURA COMPLETA

[Ver desarrollo anterior en Paso 2]

Duración: 3-5 páginas
Vinculación legal: Voluntad compartida (no contractual)

### Acuerdo Marco de Cooperación (AMC) — más formal

```
Estructura:
├─ Encabezados similares a MOU
├─ Considerandos más extensos (5-8)
├─ Cuerpo:
│  ├─ Artículos de base legal y contexto
│  ├─ Artículos específicos de cada área de cooperación
│  ├─ Compromisos detallados (con RACI)
│  ├─ Comité de Seguimiento (con reuniones mensuales)
│  ├─ Indicadores de cumplimiento cuantificables
│  ├─ Presupuesto de "gestión" (NO obligaciones financieras)
│  └─ Plazo de 3-5 años con revisión bienal

Diferencia vs MOU: Mayor formalidad, compromisos más específicos, seguimiento riguroso
Duración: 5-8 páginas
```

### Declaración Conjunta

```
Estructura más corta:
├─ Portada: "DECLARACIÓN CONJUNTA"
├─ Identificación de partes (párrafo inicial)
├─ Considerandos breves (3-4)
├─ Puntos de acuerdo (numerados, máximo 7)
├─ Compromiso de notificar al público (si aplica)
├─ Firmas de ambas partes

Propósito: Manifestar posición común sobre tema específico (política pública, evento, etc.)
Duración: 2-3 páginas
Vinculación: Declarativa, no operativa
```

---

## Paso 6 — Checklist de conformidad

### Conformidad normativa (Ley 489/1998)

- [ ] Documento identifica claramente a ambas partes (nombres legales exactos)
- [ ] Representantes tienen autoridad para firmar (cargos directivos)
- [ ] Objeto es claro y alcanzable (máximo 1 párrafo)
- [ ] Compromisos son específicos, medibles, asignables (no genéricos)
- [ ] NO hay obligaciones financieras o patrimoniales (si las hay → CONTRATO)
- [ ] Plazo de vigencia definido (no indefinido a menos que sea renovable)
- [ ] Mecanismo de seguimiento establecido (comité, reportes)
- [ ] Cláusula de no creación de obligaciones financieras (Artículo 5 o equivalente)
- [ ] Disposiciones finales completas (enmiendas, confidencialidad, PI, controversias)
- [ ] Firma de ambas partes con fecha
- [ ] Visto bueno de Jurídica (interno, no para terceros)

### Validación de contenido

- [ ] Considerandos lógicos (causa → efecto)
- [ ] Artículos numerados y sin vacíos
- [ ] Lenguaje legal pero accesible (no jerga excesiva)
- [ ] Referencias normativas exactas y vigentes
- [ ] Nombres de cargos coinciden con estructura organizacional actual
- [ ] Contactos de coordinadores válidos (correos, teléfonos)
- [ ] No hay compromisos imposibles de cumplir
- [ ] Indicadores de cumplimiento son medibles

---

## Paso 7 — Metadatos para SGDEA

### Clasificación documental

```
Tipo documental: Memorando de Entendimiento / Carta de Compromiso
Serie: Convenios y acuerdos interadministrativos
Subserie: [Cooperación bilateral / Cooperación internacional / Etc.]
Período: [Año de firma]
Fecha de firma: [DD/MM/AAAA]
Soporte: Electrónico + Original papel (si aplica)
Vigencia: [X años a partir de firma]
Versión: Original
Responsable: [Nombre y cargo — usualmente Jurídica o dependencia responsable]
Partes: [Entidad 1] y [Entidad 2]
Áreas de cooperación: [Listado de áreas]
Periodicidad de seguimiento: [Trimestral/Semestral/Anual]
Acceso: [Interno/Restringido/Público] — depende de contenido
```

---

## Paso 8 — Notas de uso y recomendaciones

### Diferencia MOU vs Contrato

```
                    MOU                        CONTRATO
─────────────────────────────────────────────────────────────
Vinculación    Voluntad, no legal           Vinculante legalmente
Dinero         NO hay transferencia         SÍ hay obligación financiera
Cumplimiento   Responsabilidad admin        Responsabilidad legal
Incumplimiento Cuestión reputacional        Acción legal / Demanda
Trámite        Simple (firma directa)       Complejo (contratación pública)
Plazo          Flexible                     Rígido
```

### Antes de firmar

1. **Revisión Jurídica OBLIGATORIA:**
   - Asesoría Jurídica de ambas entidades debe revisar
   - Validar que NO crea obligaciones financieras

2. **Autoridad de firma:**
   - Verificar que representante tiene poder para firmar MOUs
   - Si no está claro, obtener autorización de rector/director

3. **Coordinadores designados:**
   - Asegurar que coordinadores están disponibles y los contactos son válidos
   - Informarles de sus responsabilidades bajo MOU

4. **Recursos internos:**
   - Validar que la entidad tiene presupuesto/recursos para cumplir compromisos
   - Si no, NO firmar (será incumplimiento)

### Registro y distribución

- **Original firmado:** Guardar en carpeta "MOUs" de Jurídica/Secretaría General
- **Copias:** Una a cada parte, una a Jurídica, una a SGDEA
- **Publicación:** Si es público, publicar en web de la entidad (Ley 1712/2014)
- **Registro SGDEA:** Con metadatos completos y tabla de retención documental

### Seguimiento post-firma

1. Establecer recordatorios para reuniones del Comité (calendar invites)
2. Designar responsable de consolidar reportes
3. Crear carpeta compartida (si es posible) para documentación de evidencias
4. Revisar a mitad de vigencia si se requieren ajustes
5. Notificar al menos 60 días antes de vencimiento (para renovación o terminación)

### Riesgos comunes

1. **MOU sin seguimiento:** Se firma y queda guardado sin ejecutarse.
   Solución: Activar Comité de Seguimiento dentro de 30 días de firma.

2. **Compromisos ambiguos:** "Cooperar en educación" sin concretar.
   Solución: Detallar en Anexo 1 (Matriz RACI) qué hace cada parte y cuándo.

3. **Cambio de representante:** La persona que firmó se retira, nadie más conoce MOU.
   Solución: Socializar con equipo de coordinadores, no solo con representante.

4. **Obligaciones financieras ocultas:** MOU dice "no hay dinero" pero luego piden recursos.
   Solución: Revisar escrupulosamente Artículo 5 antes de firmar.

5. **Vencimiento silencioso:** MOU expira sin que nadie se dé cuenta.
   Solución: Alertas en calendario 90 días antes de vencimiento.

---

## Marco normativo embebido

Ver `references/normativa_comunicacion.md` para detalles sobre convenios interadministrativos.

**Normas principales:**

- **Ley 489/1998** — Artículos 95-96
  - Convenios interadministrativos entre entidades públicas
  - NO generan obligaciones patrimoniales
  - Son expresión de voluntad de cooperación

- **Ley 80/1993** — Estatuto de Contratación Pública
  - Aplicable si el documento genera obligaciones contractuales/financieras
  - Requisitos de proceso formal

- **Decreto 1082/2015** — Régimen de Contratación Pública
  - Procedimiento formal para contratos vs MOUs

- **Ley 594/2000** — Ley General de Archivos
  - Documentación y retención de MOUs

- **Ley 1712/2014** — Transparencia y Acceso a Información Pública
  - MOUs entre entidades públicas generalmente son públicos

- **Decreto 767/2022** — Política de Gobierno Digital
  - MOUs pueden ser digital-nativos si ambas partes aceptan

---

## Conformidad MPIA-Bogotá — Acuerdo 003/2025 CDTD

### Nivel de riesgo: **BAJO**

**Justificación:** Documento de voluntad de cooperación, no vinculante, no crea obligaciones
patrimoniales, no genera decisiones administrativas unilaterales. Expresión de intención.

### Sello de conformidad

Incluir en **firma o anexo administrativo** (NO en documento público si es bilateral):

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
AVISO DE USO DE IA — Acuerdo 003/2025 CDTD, Sección 10
Este documento fue elaborado con asistencia de inteligencia artificial
generativa. Su contenido requiere revisión, corrección y aprobación por
parte de la Asesoría Jurídica de ambas entidades antes de su firma.
La IA no sustituye el análisis legal de expertos en derecho administrativo.
Ambos firmantes asumen responsabilidad integral sobre el contenido final.
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

### Metadatos de trazabilidad IA (interno)

Guardar en expediente administrativo de la entidad:

```
--- Trazabilidad de uso de IA (Acuerdo 003/2025, Sección 10) ---
Herramienta utilizada: Skill carta-compromiso-entidad
Tipo de apoyo recibido: Generación de borrador de MOU/Carta de Compromiso
Categoría del sistema de IA: (g) Inteligencia Artificial Generativa
Nivel de riesgo MPIA: Bajo
Justificación: Documento de voluntad, no vinculante legalmente, sin decisiones autónomas
Intervención humana requerida: Revisión y aprobación jurídica de ambas partes
Fecha de generación: [DD/MM/AAAA]
Responsable de firma [Entidad 1]: [Nombre y cargo]
Responsable de firma [Entidad 2]: [Nombre y cargo]
```

### Checklist de conformidad MPIA-Bogotá (por documento)

- [ ] El MOU/Carta es BORRADOR hasta obtener firmas de ambas partes
- [ ] Asesoría Jurídica de AMBAS entidades ha revisado antes de firma
- [ ] Documento NO crea obligaciones financieras (validado en Paso 3)
- [ ] Si las crea: SUSPENDER y iniciar proceso de CONTRATO formal
- [ ] Metadatos de trazabilidad IA registrados en expediente
- [ ] No se incluyeron datos personales sensibles, información clasificada
- [ ] El contenido NO sustituye análisis legal especializado
- [ ] El contenido NO genera decisiones unilaterales vinculantes
- [ ] Ambas partes confirman validez e intención al firmar

