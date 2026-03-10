---
name: paac-entidad
description: >
  Genera Planes Anticorrupción y de Atención al Ciudadano (PAAC) para entidades del sector
  público colombiano, conforme a Ley 1474/2011 Art. 73 y Decreto 612/2018. Estructura los
  6 componentes obligatorios: gestión de riesgos de corrupción, racionalización de trámites,
  rendición de cuentas, mecanismos de atención, transparencia y acceso a información.
  Incluye matriz de riesgos, estrategias de participación ciudadana, SUIT, code of conduct.
  Output en formato Word (.docx) con cronograma y indicadores.

  Usar SIEMPRE que alguien pida: PAAC, plan anticorrupción, plan de atención al ciudadano,
  estrategia anticorrupción, Ley 1474, Decreto 612 plan 9, mapa de riesgos de corrupción,
  SUIT integrado, código de integridad, conflictos de interés, "cómo hacemos el PAAC",
  "plan de lucha contra corrupción", "estrategia de transparencia y participación", o
  cualquier variación que implique crear o actualizar un PAAC institucional.
---

# Skill: Plan Anticorrupción y de Atención al Ciudadano (PAAC)

> Esta skill genera documentos PAAC en Word (.docx), alineados con Ley 1474/2011 (Arts. 73-74),
> Decreto 612/2018 (plan 9 de 12), Decreto 1474/2011 y CONPES 3654/2010. Incluye mapa de
> riesgos de corrupción con matriz de probabilidad-impacto, estrategia de racionalización
> de trámites, rendición de cuentas (información-diálogo-incentivos), y transparencia.
> Leer `references/normativa_transparencia.md` para el detalle normativo completo.

---

## Paso 0 — Clasificación y recolección

### Preguntas obligatorias (en una sola interacción)

1. **Tipo de entidad:**
   - Entidad de orden nacional (ministerio, departamento administrativo, unidad especial)
   - Entidad territorial (gobernación, municipio, distrito)
   - Entidad descentralizada (instituto, empresa pública, fondo)
   - Otro (especificar)

2. **Vigencia del PAAC:**
   - Año(s) que cubre (ej: 2026, 2026-2028)
   - Nota: Publicación obligatoria antes del 31 de enero; seguimiento cuatrimestral

3. **¿Tiene PAAC anterior?**
   - Sí → Subir archivo anterior para validar continuidad y mejoras
   - No → Partir de cero con estructura nueva

4. **Mapa de procesos de la entidad:**
   - ¿Cuántos procesos misionales/administrativos tiene?
   - ¿Disponible en formato gráfico o listado?
   - Procesos críticos en términos de corrupción (trámites, adquisiciones, personal, información)

5. **Estructura de riesgos:**
   - ¿Tiene matriz de riesgos institucional?
   - ¿Cuáles son los 3-5 riesgos de corrupción identificados previamente?
   - ¿Hay riesgos específicos por territorio (localidad, región)?

6. **Capacidad de SUIT (Simplificación, Unificación, Informatización, Trazabilidad):**
   - ¿Cuántos trámites deberían simplificarse o eliminarse?
   - ¿Tiene sistema de información para trámites en línea?
   - ¿Grado de digitización actual (0-100%)?

7. **Participación ciudadana:**
   - ¿Tiene espacios actuales de rendición de cuentas?
   - ¿Cuántos ciudadanos/usuarios participan anualmente?
   - ¿Canales de atención al ciudadano existentes (línea PQR, portal web, presencial)?

8. **Código de integridad y conflictos de interés:**
   - ¿La entidad tiene código de conducta o código de integridad?
   - ¿Existe procedimiento de declaración de conflictos?
   - ¿Cuántos servidores públicos están obligados a declarar?

9. **Plantilla institucional:**
   - ¿Existe plantilla Word con marca, colores, estilos?
   - ¿Debe adherirse a estilo corporativo?
   - Subir archivo si existe

10. **Marco normativo adicional:**
    - ¿Hay normas específicas territoriales o sectoriales (Acuerdos, Decretos locales)?
    - ¿La entidad está sometida a supervisión especial de control?

### Preguntas opcionales

- ¿Hay iniciativas de transparencia activas (portales, índices)?
- ¿Existe presupuesto específico asignado al PAAC?
- ¿Qué indicadores clave utiliza actualmente para medir anticorrupción?

---

## Paso 1 — Estructura del documento PAAC

### Secciones del documento Word

```
Portada — Membrete, título, vigencia, fecha
Tabla de Contenido — Numerado
Prefacio — Contexto, autoridades responsables
Sección 1: Gestión del Riesgo de Corrupción
Sección 2: Racionalización de Trámites (SUIT)
Sección 3: Rendición de Cuentas
Sección 4: Mecanismos de Atención al Ciudadano
Sección 5: Transparencia y Acceso a la Información
Sección 6: Iniciativas Adicionales (Código de integridad, conflictos)
Sección 7: Indicadores, cronograma, responsables
Anexos: Matriz de riesgos, normativa, contactos
```

### Contenido detallado

**SECCIÓN 1: Gestión del Riesgo de Corrupción (Ley 1474/2011, Art. 73, Num. 1)**

- Introducción: Política de riesgo de corrupción de la entidad
- Mapa de riesgos: Identificación de procesos vulnerables (Aprobación: máximo 10 riesgos)
  * Para cada riesgo: Proceso | Descripción del riesgo | Causa(s) | Consecuencia(s) esperada(s)
  * Probabilidad (1-5) × Impacto (1-5) → Zona de riesgo (Rojo/Amarillo/Verde)
  * Controles existentes | Controles nuevos propuestos | Responsable | Plazo
- Matriz de riesgos (tabla detallada — ver Paso 2)
- Responsable de coordinación: Oficina de Control Interno / Comité de Ética
- Meta: Reducir en X% cantidad de riesgos Rojo a Amarillo o Verde en vigencia

**SECCIÓN 2: Racionalización de Trámites (SUIT — Decreto 2150/1995)**

- Diagnóstico actual: Número de trámites, complejidad, tiempo promedio
- Estrategia SUIT:
  * Simplificación: Trámites que se pueden agilizar (descripción, ahorro tiempo/costo)
  * Unificación: Trámites que pueden combinarse en uno
  * Informatización: Trámites candidatos a digitalización
  * Trazabilidad: Implementación de seguimiento ciudadano
- Listado de 3-5 trámites piloto para rediseño
- Cronograma de implementación (trimestral)
- Responsable: Oficina de Gestión de Procesos o equivalente

**SECCIÓN 3: Rendición de Cuentas (CONPES 3654/2010)**

Tres elementos obligatorios:

a) **Información:** ¿Qué publica la entidad y cómo?
   - Información que la entidad publica de forma activa
   - Canales: Portal web, redes sociales, asambleas, actas
   - Periodicidad: Mensual, trimestral, anual
   - Responsable de publicación

b) **Diálogo:** ¿Cómo interactúa con ciudadanía?
   - Espacios presenciales: N° de cabildos abiertos, espacios de participación
   - Espacios virtuales: Foros en línea, consultas públicas
   - Mecanismo de retroalimentación ciudadana
   - Cronograma anual de espacios

c) **Incentivos:** ¿Cómo se promueve la participación?
   - Reconocimiento público a participantes
   - Mecanismos de participación ciudadana en evaluación de gestión
   - N° esperado de participantes por evento

**SECCIÓN 4: Mecanismos de Atención al Ciudadano (Ley 1474/2011, Art. 73, Num. 4)**

- Sistema de PQRSDF: Descripción de canales (presencial, telefónico, web, correo)
- Indicadores de atención:
  * N° promedio de PQRSDF mensual
  * Tiempo promedio de respuesta (días)
  * % de respuestas oportunas (meta: 95%)
  * Nivel de satisfacción (encuesta anual)
- Mejoras propuestas en vigencia (2-3 iniciativas)
- Responsable: Oficina de Atención al Ciudadano

**SECCIÓN 5: Transparencia y Acceso a la Información (Ley 1712/2014)**

- Política de transparencia activa:
  * Información mínima obligatoria (Art. 9-11, Ley 1712)
  * Esquema de publicación (Art. 12)
  * Responsable de cada tipo de información
  * Periodicidad de actualización
- Protección de información clasificada y reservada (Ley 1712, Cap. 3)
- Atención de solicitudes de información pública:
  * N° esperado anual
  * Plazo de respuesta (máximo 10 días hábiles)
  * Procedimiento de recursos
- Índice de Transparencia (si aplica): Evaluación externa anual
- Responsable: Oficina de Información Pública / Comunicaciones

**SECCIÓN 6: Iniciativas Adicionales**

a) **Código de Integridad:**
   - Valores institucionales: Transparencia, honestidad, legalidad, eficiencia
   - Deberes: Servidores públicos, contratistas, proveedores
   - Sanciones por incumplimiento
   - Responsable de difusión y monitoreo

b) **Conflictos de Interés:**
   - Política de declaración de conflictos (anual)
   - Procedimiento de investigación ante denuncias
   - N° de declaraciones esperadas vs. recibidas
   - Casos investigados y acciones disciplinarias

c) **Iniciativa de Cero Tolerancia:**
   - Denuncia anónima de actos de corrupción
   - Investigación y resultado
   - Protección a denunciantes

---

## Paso 2 — Matriz de Riesgos de Corrupción (Sección 1, Anexo)

### Columnas obligatorias

```
A. Proceso
   Ej: "Contratación de bienes y servicios", "Selección de personal"

B. Descripción del riesgo
   Ej: "Favoritismo en adjudicación de contrato", "Soborno en proceso de selección"

C. Causa potencial
   Ej: "Criterios de selección débiles", "Falta de supervisión"

D. Consecuencia esperada
   Ej: "Gasto innecesario", "Contratación de personal incompetente"

E. Probabilidad (1-5)
   1 = Muy baja (casi nunca ocurre)
   5 = Muy alta (ocurre frecuentemente)

F. Impacto (1-5)
   1 = Insignificante (costo <$1M)
   5 = Catastrófico (costo >$50M, reputación)

G. Nivel de Riesgo (= E × F)
   Rango: 1-25 (categorizar: Rojo = 20-25, Amarillo = 10-19, Verde = 1-9)

H. Control(es) existente(s)
   Ej: "Revisión por superior", "Auditoría interna trimestral"

I. Efectividad del control (%)
   0-100%, evaluación subjetiva del control actual

J. Controles nuevos propuestos
   Ej: "Implementar sistema de doble aprobación", "Capacitación en ética"

K. Plazo de implementación (meses)
   1, 3, 6, 12

L. Responsable
   Cargo y/o dependencia responsable de control

M. Observaciones
   Campo libre para contexto adicional
```

### Ejemplo de matriz

| Proceso | Riesgo | Probabilidad | Impacto | Nivel | Control actual | Control nuevo | Plazo | Responsable |
|---------|--------|--------------|---------|-------|-----------------|---|---|---|
| Adquisición de tecnología | Sobreprecio en compras | 4 | 4 | Rojo (16) | Cotización de 3 proveedores | Sistema e-procurement obligatorio | 6 meses | Jefe de Compras |
| Selección de personal | Nepotismo | 2 | 3 | Amarillo (6) | Comisión de selección | Validación externa + acta pública | 3 meses | RRHH |
| Ejecución presupuestal | Malversación | 1 | 5 | Amarillo (5) | Auditoría anual | Auditoría semestral + alertas | 1 mes | Tesorería |

---

## Paso 3 — Cronograma de implementación

### Formato tabla en documento

```
Actividad | Componente | Responsable | Mes 1 | Mes 2 | Mes 3 | ... | Mes 12 | Estado
Publicación PAAC | Transparencia | Comunicaciones | X | | | | | Planificado
Capacitación en ética | Código integridad | RRHH + Bienestar | | X | X | | | En progreso
Rediseño trámites piloto | SUIT | Procesos | | | X | X | X | X | Planificado
Encuesta participación ciudadana | Rendición de cuentas | Atención ciudadano | | | | | X | Planificado
```

---

## Paso 4 — Indicadores del PAAC (Sección 7)

### Matriz de indicadores

| Componente | Indicador | Fórmula | Meta 2026 | Línea base | Responsable | Periodicidad |
|---|---|---|---|---|---|---|
| Riesgos | % Riesgos Rojo vs. Amarillo/Verde | (Riesgos Rojo / Total riesgos) × 100 | ≤20% | 40% | Control Interno | Trimestral |
| SUIT | N° trámites digitalizados | Trámites en línea / Trámites totales | ≥5 | 2 | Procesos | Semestral |
| Rendición | N° espacios de participación | Asambleas + cabildos realizados | ≥4 | 1 | Atención ciudadano | Anual |
| Transparencia | % Información actualizada | Datos con <30 días antigüedad / Total | ≥95% | 75% | Comunicaciones | Mensual |
| PQRSDF | % Respuestas oportunas | PQRSDF respondidas ≤10 días / Total | ≥95% | 80% | Atención ciudadano | Mensual |
| Integridad | N° capacitaciones en ética | Eventos realizados | ≥2 | 0 | RRHH | Anual |

---

## Paso 5 — Checklist de conformidad normativa

### Conformidad Ley 1474/2011 y Decreto 612/2018

- [ ] Documento contiene los 6 componentes obligatorios (Arts. 73-74)
- [ ] Matriz de riesgos con mínimo 5 riesgos identificados
- [ ] Estrategia SUIT con mínimo 3 trámites para rediseño
- [ ] Elementos de rendición de cuentas: Información, Diálogo, Incentivos
- [ ] Sistema de PQRSDF descrito y con indicadores
- [ ] Política de transparencia alineada con Ley 1712/2014
- [ ] Código de integridad / conducta incluido o referenciado
- [ ] Procedimiento de conflictos de interés descrito
- [ ] Cronograma de implementación con responsables
- [ ] Indicadores con metas cuantificables
- [ ] Responsable de coordinación del PAAC designado
- [ ] Publicación programada para antes del 31 de enero
- [ ] Seguimiento cuatrimestral planificado (abril 30, agosto 31, diciembre 31)
- [ ] Alineación con Decreto 612/2018 (plan 9 de 12 planes) validada
- [ ] Formato .docx con membrete institucional
- [ ] Tabla de contenido automática
- [ ] Trazabilidad de versiones

### Validaciones de contenido

- [ ] Responsables identificables (cargo, correo, teléfono)
- [ ] Metas SMART (Específicas, Medibles, Alcanzables, Relevantes, con Tiempo)
- [ ] No hay referencias vagas ("mejorar", "fortalecer" sin métrica)
- [ ] Matriz de riesgos tiene evidencia de participación de áreas clave
- [ ] Cronograma es realista vs. capacidades institucionales

---

## Paso 6 — Metadatos SGDEA

```
Tipo documental: Plan estratégico / Plan de Lucha contra la Corrupción
Serie: Planes institucionales de prevención
Subserie: PAAC
Período: [Vigencia, ej: 2026]
Fecha elaboración: DD/MM/AAAA
Fecha de aprobación: DD/MM/AAAA
Soporte: Electrónico (Word .docx)
Vigencia documental: [N años según norma local]
Clasificación: Información de interés público (Ley 1712)
Alineación normativa: Ley 1474/2011, Decreto 612/2018, Ley 1712/2014
Responsable de seguimiento: Oficina de Control Interno / Jefe PAAC
Publicación requerida: Sí — Web pública antes del 31 de enero
Periodicidad de actualización: Cuatrimestral (seguimiento) + anual (revisión integral)
Acceso: Público (salvo información reservada Art. 19, Ley 1712)
Versión: v01 (para primera elaboración)
```

---

## Paso 7 — Marco normativo embebido

Ver `references/normativa_transparencia.md` para artículos completos.

**Normas principales:**

- **Ley 1474 de 2011** — Estatuto Anticorrupción
  - Arts. 73-74: Componentes obligatorios del PAAC
  - Art. 75: Publicación antes del 31 de enero

- **Decreto 612 de 2018** — Integración de Planes Estratégicos
  - Plan 9 de 12: PAAC como plan integrado obligatorio
  - Aplica a orden nacional y territorial

- **Ley 1712 de 2014** — Ley de Transparencia y Acceso a Información
  - Cap. 1: Esquema de publicación activa
  - Cap. 2: Atención de solicitudes de información pública

- **CONPES 3654 de 2010** — Política de Rendición de Cuentas
  - Tres elementos: Información, Diálogo, Incentivos

- **Decreto 2150 de 1995** — Simplificación de Trámites (SUIT)
  - Actualización: Decreto 1081/2015 (Código de Procedimiento Administrativo)

---

## Paso 8 — Notas de uso

### Finalidad del PAAC

El PAAC es un **documento de planificación** que evidencia el compromiso institucional de
la entidad frente a anticorrupción y transparencia. No es un instrumento de control operativo
(ese es el Sistema de Control Interno — ver skill `informe-control-interno-entidad`).

### Audiencia y distribución

- **Destinatarios:** Junta Directiva / Consejo Directivo, servidores públicos, ciudadanía
- **Publicación obligatoria:** Portal web de la entidad, pestaña "Transparencia"
- **Referencia externa:** Supervisores (Contraloría, Procuraduría, Defensoría, entes sectoriales)

### Relación con otros documentos

- **Decreto 612/2018 (12 planes):** El PAAC integra componentes de múltiples planes
  (Transparencia, Gestión de Talento Humano, Seguridad de Información)
- **Informe de Gestión:** Reporta avance en cumplimiento de metas PAAC (trimestral/anual)
- **Sistema de Control Interno:** Auditadas en informes de control interno

### Recomendaciones operativas

1. **Participación multidisciplinaria:** El PAAC debe ser construido con Control Interno,
   RRHH, Procesos, Comunicaciones, Atención al Ciudadano. No es tarea solo de Control.

2. **Validación del mapa de riesgos:** Asegurar que los riesgos identificados sean reales
   (no teóricos). Usar experiencias de auditorías, investigaciones disciplinarias previas.

3. **Realismo en metas:** Si el PAAC promete 10 mejoras pero solo tiene presupuesto/capacidad
   para 3, será una herramienta inútil. Mejor 3 metas alcanzables que 10 inalcanzables.

4. **Difusión:** Publicar un "PAAC ciudadano" (versión simplificada) para facilitar
   comprensión pública de los compromisos.

5. **Seguimiento:** El PAAC debe actualizarse cuatrimestralmente (no esperar a fin de año).

---

## MPIA Conformity Block — Acuerdo 003/2025 CDTD, Sección 10

### Sello de conformidad del documento

Incluir al final del documento o en pie de página:

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

### Nivel de riesgo MPIA

**BAJO**

Justificación: El PAAC es un documento de planificación estratégica que define compromisos
y estrategias institucionales de lucha contra corrupción. No genera decisiones autónomas,
no interactúa directamente con ciudadanía de forma vinculante, y no sustituye juicio técnico
de funcionarios especializados. Requiere aprobación de liderazgo institucional.

### Metadatos de trazabilidad IA

Incluir en metadatos SGDEA del documento:

```
--- Trazabilidad de uso de IA (Acuerdo 003/2025, Sección 10) ---
Herramienta utilizada: Claude / Skill paac-entidad (Cowork)
Tipo de apoyo recibido: Estructuración de plan anticorrupción; síntesis normativa
Categoría del sistema de IA: (g) Inteligencia Artificial Generativa
Nivel de riesgo MPIA: Bajo
Justificación del nivel: Asistencia en estructuración de documento estratégico de
  planificación institucional. Decisiones de política pública corresponden a
  funcionarios y liderazgo institucional.
Intervención humana requerida: Revisión completa, corrección de datos, aprobación
  por Junta/Consejo Directivo
Fecha de generación: DD/MM/AAAA
Funcionario responsable: [Nombre, cargo, correo del Jefe PAAC o equivalente]
```

### Checklist de conformidad MPIA-Bogotá (por documento)

**Conformidad Acuerdo 003/2025 — Uso cotidiano de IA (Sección 10):**

- [ ] El documento es un BORRADOR que requiere aprobación humana
- [ ] Pie de página con aviso de uso de IA incluido
- [ ] Metadatos de trazabilidad IA incluidos
- [ ] No se ingresaron datos personales sensibles, información reservada o clasificada
- [ ] El contenido NO sustituye análisis de riesgos específicos de la entidad
- [ ] El contenido NO genera actos administrativos vinculantes (es estrategia)
- [ ] El liderazgo institucional revisará y validará antes de publicación
- [ ] La aprobación será registrada con firma en acta de Junta/Consejo

