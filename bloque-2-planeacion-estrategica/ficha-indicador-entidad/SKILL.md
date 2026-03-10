---
name: ficha-indicador-entidad
description: >
  Genera Fichas Técnicas de Indicador para entidades del sector público colombiano,
  alineadas con MIPG (Modelo Integrado de Planeación y Gestión) y normativa de
  evaluación de resultados. Output: .docx con elementos SMART, semáforo de desempeño,
  y análisis de tendencias. Soporta modo individual y batch.

  Usar SIEMPRE que alguien pida: ficha técnica de indicador, ficha de indicador,
  indicador MIPG, documentar indicador, hoja de vida del indicador, indicador de
  gestión, indicador de eficacia, indicador de eficiencia, indicador de producto,
  indicador de resultado, "cómo formulo un indicador", "necesito la ficha del
  indicador", o cualquier variación que implique crear la ficha técnica de un
  indicador de gestión para una entidad pública colombiana.
---

# Generador de Fichas Técnicas de Indicador — MIPG

## Descripción General

Este skill genera **Fichas Técnicas de Indicador** para entidades del sector público
colombiano. Cada ficha documenta un indicador de desempeño alineado con:

- **MIPG**: Modelo Integrado de Planeación y Gestión (Decreto 1499/2017)
- **SMART**: Indicadores Específicos, Medibles, Alcanzables, Relevantes y Acotados en tiempo
- **SGDEA**: Sistema de Gestión Documental de Entidades Públicas
- **PDD**: Plan de Desarrollo Departamental (si aplica)
- **Normativa**: Decreto 1499/2017, Manual Operativo MIPG (DAFP), Ley 489/1998, GTC-185

Output: documentos `.docx` listos para publicación interna y cumplimiento normativo.

---

## PASO 0: Clasificación y Recolección de Información

### 0.1 Información de la Entidad

Antes de iniciar, se recopila:

1. **Nombre de la entidad** (obligatorio)
   - Ej: "Alcaldía Municipal de Medellín", "Instituto Colombiano de Bienestar Familiar"

2. **Dependencia / Área responsable** (obligatorio)
   - Ej: "Dirección de Evaluación de Gestión", "Subdirección de Calidad"

3. **Tipo de entidad** (obligatorio)
   - [ ] Nacional / Central
   - [ ] Territorial (Gobernación, Municipio, Distrito)
   - [ ] Descentralizada (Instituto, Fondo, Empresa Industrial y Comercial)

4. **¿Dispone de plantilla .docx institucional?** (recomendado)
   - Si SÍ → Usuario carga archivo (.docx, máx 5 MB)
   - Si NO → Se usa plantilla estándar predefinida

5. **Cantidad de indicadores a documentar** (obligatorio)
   - [ ] Uno (1) — Operación individual
   - [ ] Múltiples — Batch (2-30 indicadores con mismo formato)

6. **Modo de operación** (obligatorio)
   - [ ] Individual: 1 indicador, documento independiente
   - [ ] Batch: N indicadores, un documento por indicador o único documento consolidado

---

## PASO 1: Estructura del Documento (Elementos Obligatorios)

Cada Ficha Técnica de Indicador contiene **11 campos obligatorios** y campos opcionales/contextuales:

### Sección A: Identificación del Indicador

| Campo | Descripción | Ejemplo |
|-------|-------------|---------|
| **Nombre del Indicador** | Denominación clara y única | "Porcentaje de satisfacción de usuarios en trámites virtuales" |
| **Código del Indicador** | Identificador único (formato: ENTI-IND-XXX) | ALCM-IND-2026-001 |
| **Objetivo del Indicador** | Qué se mide y por qué (máx 200 caracteres) | "Evaluar el nivel de satisfacción de ciudadanos que realizan trámites mediante plataformas digitales" |
| **Tipo de Indicador** | Clasificación según Decreto 1499/2017 | Eficacia / Eficiencia / Efectividad / Gestión / Producto / Resultado |

### Sección B: Definición Técnica

| Campo | Descripción | Requerimientos SMART |
|-------|-------------|---------------------|
| **Fórmula de Cálculo** | Expresión matemática clara | (Usuarios satisfechos / Total usuarios encuestados) × 100 |
| **Unidad de Medida** | Formato cuantificable | Porcentaje (%) / Número / Moneda (COP) / Índice / Tasa |
| **Línea Base** | Valor inicial de referencia (año, valor) | 2025: 65% |
| **Meta Anual** | Valor esperado para el período | 80% |
| **Metas Periódicas** | Desglose (trimestral, semestral) | Q1: 70%, Q2: 75%, Q3: 77%, Q4: 80% |

### Sección C: Operación y Responsabilidad

| Campo | Descripción | Observaciones |
|-------|-------------|---------------|
| **Fuente de Datos** | Origen de información (sistema, encuesta, base datos) | "Plataforma de satisfacción web — módulo de reportes" |
| **Frecuencia de Medición** | Periodicidad de actualización | Mensual / Trimestral / Semestral / Anual |
| **Responsable del Indicador** | Cargo y dependencia | "Analista de Calidad — Dirección de Evaluación" |
| **Observaciones / Análisis de Desviaciones** | Explicación de brechas vs. meta | Campo dinámico, se actualiza con cada medición |

---

## PASO 2: Adaptación Según Tipo de Indicador

Cada ficha se adapta automáticamente:

### 2.1 Indicadores de Eficacia
- Foco: ¿Se logró el objetivo planificado?
- Semáforo: Verde ≥90%, Amarillo 70-89%, Rojo <70%
- Análisis: Comparación meta vs. resultado

### 2.2 Indicadores de Eficiencia
- Foco: ¿Con qué recursos se logró?
- Semáforo: Verde ≥90%, Amarillo 70-89%, Rojo <70%
- Análisis: Costo unitario, productividad

### 2.3 Indicadores de Efectividad
- Foco: ¿Qué impacto real tuvo?
- Semáforo: Verde ≥80%, Amarillo 50-79%, Rojo <50%
- Análisis: Beneficiarios, cobertura, impacto

### 2.4 Indicadores de Gestión
- Foco: Procesos y procedimientos internos
- Semáforo: Verde ≥85%, Amarillo 60-84%, Rojo <60%
- Análisis: Conformidad vs. estándares operacionales

### 2.5 Indicadores de Producto/Resultado
- Foco: Outputs entregables
- Semáforo: Verde ≥100% de meta, Amarillo 80-99%, Rojo <80%
- Análisis: Volumen, calidad, oportunidad

---

## PASO 3: Elementos Adicionales y Contexto MIPG

### 3.1 Campos Contextuales (si aplica)

- **Proceso Asociado**: Referencia a mapa de procesos (SIG institucional)
- **Dimensión MIPG**: Dirección Estratégica / Evaluación de Resultados / Capacidad Organizacional / Información y Comunicación / Procesos
- **Política MIPG**: Plan estratégico, Plan de Acción, PEI
- **Vinculación PDD**: Si es entidad territorial (Gobernación, Municipio)
  - Programa PDD asociado
  - Objetivo sectorial alineado

### 3.2 Tabla de Seguimiento Trimestral (integrada en ficha)

| Período | Meta | Resultado | % Cumplimiento | Semáforo | Observaciones |
|---------|------|-----------|-----------------|----------|---------------|
| Q1 2026 | 70% | —         | —              | ⚪       | Por medir    |
| Q2 2026 | 75% | —         | —              | ⚪       | Por medir    |
| Q3 2026 | 77% | —         | —              | ⚪       | Por medir    |
| Q4 2026 | 80% | —         | —              | ⚪       | Por medir    |

Semáforo: 🟢 Verde | 🟡 Amarillo | 🔴 Rojo | ⚪ Sin dato

### 3.3 Análisis de Tendencias

Sección de comparación histórica (últimos 3 períodos):

- Gráfico de línea: Tendencia del indicador
- Tabla: Variación período a período (Δ absoluta y %)
- Interpretación: ¿Mejora, estable o deterioro?

---

## PASO 4: Plantilla .docx — Especificaciones de Formato

### 4.1 Estructura Visual

```
┌────────────────────────────────────────┐
│  ENCABEZADO: Logo entidad + Título    │
│  Ficha Técnica de Indicador [Código]   │
│  Año: 2026 | Elaborado: [Fecha]        │
└────────────────────────────────────────┘

SECCIÓN A: IDENTIFICACIÓN
├─ Nombre del Indicador
├─ Código
├─ Objetivo
└─ Tipo

SECCIÓN B: DEFINICIÓN TÉCNICA
├─ Fórmula de Cálculo
├─ Unidad de Medida
├─ Línea Base
├─ Meta Anual
└─ Metas Periódicas

SECCIÓN C: OPERACIÓN
├─ Fuente de Datos
├─ Frecuencia de Medición
├─ Responsable
└─ Observaciones

SECCIÓN D: CONTEXTO MIPG
├─ Proceso Asociado
├─ Dimensión MIPG
├─ Política MIPG
└─ Vinculación PDD (si aplica)

SECCIÓN E: SEGUIMIENTO
├─ Tabla Trimestral
└─ Análisis de Tendencias
```

### 4.2 Estilos y Formatos

- **Fuente**: Calibri 11 pt (encabezados: 14 pt, negrita)
- **Colores semáforo**: Verde (#00B050), Amarillo (#FFD966), Rojo (#FF0000)
- **Márgenes**: 2.54 cm (superior/inferior), 2.0 cm (laterales)
- **Espaciado líneas**: 1.15 (legibilidad)
- **Numeración**: Automática (Nivel 1: apartados, Nivel 2: ítems)

### 4.3 ¿Dispone de plantilla institucional?

- **SI**: Usuario carga archivo .docx. Sistema integra datos en estilos existentes.
- **NO**: Sistema usa plantilla estándar MIPG predefinida.

---

## PASO 5: Checklist de Conformidad + Metadatos SGDEA

### 5.1 Validación MIPG

Antes de generar .docx, se verifica:

- [ ] Indicador es SMART (Específico, Medible, Alcanzable, Relevante, Acotado en tiempo)
- [ ] Fórmula de cálculo es clara y reproducible
- [ ] Meta es realista (comparada vs. línea base)
- [ ] Frecuencia de medición es operativa
- [ ] Responsable está identificado con cargo
- [ ] Proceso asociado existe en mapa de procesos

### 5.2 Metadatos SGDEA (según GTC-185 y normas archivísticas)

Cada documento .docx incluye propiedades:

| Propiedad | Valor | Ejemplo |
|-----------|-------|---------|
| **Título** | Nombre del indicador | "Porcentaje de satisfacción de usuarios" |
| **Asunto** | "Ficha Técnica de Indicador — MIPG" | — |
| **Autor** | Responsable / Entidad | "Alcaldía Municipal de Medellín" |
| **Palabras clave** | Indicador, MIPG, desempeño, sector público | — |
| **Categoría** | "Evaluación de Resultados" | — |
| **Clasificación SGDEA** | Código de clasificación documental | GERE.020 (Gestión y Evaluación de Resultados) |
| **Vigencia documental** | Período de retención | 5 años (según Decreto 1499/2017) |

---

## Flujo de Interacción

### 1. **Inicio**
   - Usuario invoca skill: "Genera ficha técnica de indicador"
   - Sistema pregunta: Entidad, dependencia, cantidad de indicadores, modo (individual/batch)

### 2. **Carga de Plantilla (opcional)**
   - Si usuario tiene .docx institucional → carga archivo
   - Sistema valida formato (max 5 MB, extensión .docx)

### 3. **Recopilación de Datos del Indicador**
   - Nombre, objetivo, tipo, fórmula, unidad, línea base, meta, fuente, frecuencia, responsable
   - Campos contextuales: Proceso, Dimensión MIPG, vinculación PDD

### 4. **Validación SMART**
   - Sistema verifica criterios SMART
   - Si hay desviaciones → sugiere correcciones

### 5. **Generación de .docx**
   - Completa ficha con plantilla (institucional o estándar)
   - Aplica semáforo según tipo de indicador
   - Integra tabla de seguimiento y análisis de tendencias

### 6. **Entrega**
   - Descargable: `[Código_Indicador]_FichaTecnica_2026.docx`
   - En modo batch: Archivo consolidado o ZIP con múltiples fichas

---

## Referencias Normativas

- **Decreto 1499/2017**: Modelo Integrado de Planeación y Gestión (MIPG)
  - Dimensión 4: Evaluación de Resultados
  - Requisitos para indicadores de desempeño
- **Manual Operativo MIPG (DAFP)**: Lineamientos SMART y construcción de indicadores
- **Ley 489/1998**: Marco de la administración pública
- **GTC-185 (ICONTEC)**: Directrices para gestión de documentos electrónicos
- **Política de Archivo (Ley 594/2000)**: Normas de clasificación documental

Ver: `references/normativa_planeacion.md` (en repositorio del skill)

---

## Notas Operativas

- **Idioma**: Español (nomenclatura colombiana, formatos locales)
- **Zona horaria**: Colombia (UTC-5)
- **Moneda**: COP (cuando sea aplicable)
- **Ciclo fiscal**: Año calendario (enero-diciembre)
- **Soporte batch**: Máximo 30 indicadores por sesión; más allá, agendar segunda sesión

---

**Última actualización**: 9 de marzo de 2026
**Versión**: 1.0 — Producción

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
Justificación del nivel: Documentación de indicadores de gestión. Sin decisiones, sin datos sensibles.
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
