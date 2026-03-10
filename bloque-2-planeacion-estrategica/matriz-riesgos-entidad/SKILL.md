---
name: matriz-riesgos-entidad
description: >
  Genera matrices de riesgos para entidades del sector público colombiano, alineadas
  con MIPG Dimensión 7 (Control Interno), la Guía de Administración del Riesgo del
  DAFP y la Ley 1474/2011. Salida en formato .xlsx con 4 hojas: Matriz de Riesgos,
  Mapa de Calor 5×5, Plan de Tratamiento y Seguimiento. Soporta riesgos de gestión,
  corrupción, seguridad digital y fiscal.

  Usar SIEMPRE que alguien pida: matriz de riesgos, mapa de riesgos, mapa de calor,
  gestión de riesgos, riesgos de corrupción, riesgos institucionales, plan anticorrupción,
  riesgo operativo, análisis de riesgos DAFP, "necesito la matriz de riesgos del proceso",
  "riesgos para el plan anticorrupción", o cualquier variación que implique identificar,
  analizar y valorar riesgos de una entidad pública colombiana.
---

# Matriz de Riesgos para Entidades Públicas Colombianas

**Objetivo:** Generar una matriz de riesgos estructurada, integrada y documentada que cumpla con normativa colombiana (MIPG Dimensión 7, DAFP, Ley 1474/2011) para entidades del sector público.

> Leer `references/normativa_planeacion.md` para el detalle de la metodología DAFP 5×5, escalas de probabilidad e impacto, y mapa de calor.

**Normativa aplicable:**
- Decreto 1499/2017 (MIPG Dimensión 7: Control Interno)
- Guía de Administración del Riesgo — DAFP (metodología 5×5)
- Ley 1474/2011 (Estatuto Anticorrupción; Plan de Acción Anticorrupción)
- Decreto 612/2018 (Integración Plan Anticorrupción)
- NTC-ISO 31000:2018 (Principios y Marco de Gestión de Riesgos)
- GTC-185 (Guía de Gestión de Riesgos)

---

## PASO 0: Clasificación y Recolección de Información

Antes de iniciar la generación de la matriz, necesito confirmar los siguientes datos:

### Datos obligatorios

1. **Nombre de la entidad:** (Ej: "Alcaldía Municipal de Bogotá", "DAFP", "Corporación Autónoma Regional")
2. **Tipo de entidad:** (Selecciona uno)
   - [ ] Ministerio o Departamento Administrativo
   - [ ] Entidad Territorial (Gobernación, Alcaldía)
   - [ ] Empresa Comercial Estatal
   - [ ] Entidad Descentralizada (autónoma, sector descentralizado)
   - [ ] Otra (especifica)

3. **Proceso(s) a analizar:** (Listado: procesos misionales, de apoyo, o direccionamiento estratégico)
   - Ejemplo: "Contratación pública", "Tesorería", "Gestión de Talento Humano"

4. **Tipo(s) de riesgo a incluir:**
   - [ ] Riesgo de Gestión (Operativo) — **obligatorio**
   - [ ] Riesgo de Corrupción (Ley 1474/2011) — obligatorio si hay Plan Anticorrupción
   - [ ] Riesgo de Seguridad Digital (MINTIC)
   - [ ] Riesgo Fiscal (MHCP)

5. **¿Existe Plan de Acción Anticorrupción (PAA)?** (Sí/No)
   - Si es **Sí:** la matriz incluirá riesgos de corrupción + tratamientos integrados.

6. **¿Tienes plantilla .xlsx preexistente?** (Sí/No)
   - Si es **Sí:** sube el archivo para adaptarlo.

---

## PASO 1: Estructura del Documento (.xlsx)

El archivo de salida contendrá **4 hojas (sheets)** con la siguiente estructura:

### Sheet 1: "Matriz de Riesgos" (Registro Principal)

**Columnas (A–S):**

| # | Columna | Tipo | Descripción |
|---|---------|------|-------------|
| A | N° | Número | Identificador secuencial del riesgo |
| B | Proceso | Texto | Nombre del proceso afectado |
| C | Objetivo del Proceso | Texto | Objetivo estratégico del proceso |
| D | Tipo de Riesgo | Desplegable | Gestión / Corrupción / Seguridad Digital / Fiscal |
| E | Descripción del Riesgo | Texto | Qué puede salir mal |
| F | Causa (Raíz) | Texto | Por qué ocurriría el riesgo |
| G | Consecuencia | Texto | Qué pasaría si se materializa |
| H | Probabilidad (Inherente) | Número 1–5 | Escala DAFP: 1=Rara vez, 5=Casi seguro |
| I | Impacto (Inherente) | Número 1–5 | Escala DAFP: 1=Insignificante, 5=Catastrófico |
| J | Zona de Riesgo (Inherente) | Texto | Resultado del mapa de calor |
| K | Control Existente | Texto | Control actual que mitiga el riesgo |
| L | Tipo de Control | Desplegable | Preventivo / Detectivo / Correctivo |
| M | Probabilidad Residual | Número 1–5 | Prob. después del control |
| N | Impacto Residual | Número 1–5 | Impacto después del control |
| O | Zona Residual | Texto | Zona después de aplicar control |
| P | Tratamiento | Desplegable | Evitar / Reducir / Compartir / Aceptar |
| Q | Responsable | Texto | Nombre y cargo del responsable |
| R | Fecha de Seguimiento | Fecha | Próxima revisión |
| S | Observaciones | Texto | Notas adicionales |

---

### Sheet 2: "Mapa de Calor" (Visualización 5×5)

**Matriz de Zona según Probabilidad (filas 1–5) e Impacto (columnas 1–5):**

| | 1 (Insignificante) | 2 (Menor) | 3 (Moderado) | 4 (Mayor) | 5 (Catastrófico) |
|---|---|---|---|---|---|
| **5 (Casi seguro)** | Alta | Alta | Extrema | Extrema | Extrema |
| **4 (Probable)** | Moderada | Alta | Alta | Extrema | Extrema |
| **3 (Posible)** | Baja | Moderada | Alta | Extrema | Extrema |
| **2 (Improbable)** | Baja | Baja | Moderada | Alta | Extrema |
| **1 (Rara vez)** | Baja | Baja | Moderada | Alta | Alta |

**Colorimetría (Formato Condicional):**
- **Baja:** Verde claro (#C6EFCE)
- **Moderada:** Amarillo (#FFEB9C)
- **Alta:** Naranja (#FFC7CE)
- **Extrema:** Rojo oscuro (#C00000)

---

### Sheet 3: "Plan de Tratamiento"

**Columnas (A–H):**

| # | Columna | Descripción |
|---|---------|-------------|
| A | N° Riesgo | FK a Sheet 1 |
| B | Descripción del Riesgo | Referencia |
| C | Tratamiento Asignado | Evitar / Reducir / Compartir / Aceptar |
| D | Acción de Tratamiento | Descripción de la medida |
| E | Responsable | Persona designada |
| F | Fecha Inicio | Planificada |
| G | Fecha Finalización | Esperada |
| H | Estado | Planificado / En Ejecución / Completado / Suspendido |

---

### Sheet 4: "Seguimiento"

**Columnas (A–G):**

| # | Columna | Descripción |
|---|---------|-------------|
| A | N° Riesgo | FK a Sheet 1 |
| B | Descripción del Riesgo | Referencia |
| C | Zona Inherente | Histórico |
| D | Zona Actual (post-control) | Estado presente |
| E | Tendencia | Aumentando / Estable / Disminuyendo |
| F | Fecha Última Revisión | Cuándo se actualizó |
| G | Próxima Revisión | Periodicidad (trimestral, semestral) |

---

## PASO 2: Adaptación según Tipo de Riesgo

Dependiendo de los tipos seleccionados en Paso 0, se incluirán criterios específicos:

### Riesgo de Gestión (Operativo)
- Cobertura: procesos misionales y de apoyo.
- Enfoque: disponibilidad, calidad, eficiencia.
- Controles: internos de proceso, validaciones, auditorías internas.

### Riesgo de Corrupción (Ley 1474/2011)
- Obligatorio si existe Plan de Acción Anticorrupción (PAA).
- Procesos de alto riesgo: contratación, tesorería, asignación de beneficios.
- Controles: segregación de funciones, trazabilidad, vigilancia (auditoría).
- Tratamiento: medidas de transparencia, denuncias (LÍNEA ÉTICA).

### Riesgo de Seguridad Digital (MINTIC)
- Procesos críticos: bases de datos, sistemas de información, datos personales.
- Controles: encriptación, autenticación, respaldos, recuperación ante desastres.
- Normativa: Decreto 1377/2013 (Protección de Datos Personales).

### Riesgo Fiscal (MHCP)
- Procesos: presupuesto, recaudos, transferencias.
- Controles: validaciones de cálculo, conciliaciones contables, auditoría fiscal.

---

## PASO 3: Plantilla y Formato Técnico

### Si el usuario tiene plantilla preexistente (.xlsx):
- Cargar y validar que contenga columnas mínimas (Proceso, Descripción, Probabilidad, Impacto).
- Adaptar estructura para incluir hojas faltantes (Mapa de Calor, Plan de Tratamiento, Seguimiento).
- Preservar datos históricos.

### Si no tiene plantilla:
- **Crear desde cero** con estructura estándar (4 hojas, formato descrito en Paso 1).

### Especificaciones técnicas:
- **Formato:** Microsoft Excel 2016+ (.xlsx)
- **Fuente:** Calibri 11 pt
- **Encabezados:** Negrita, fondo gris claro (#D3D3D3)
- **Filas de datos:** Blanca con bordes simples
- **Números:** Alineados a la derecha; fechas en formato DD/MM/YYYY
- **Ancho de columnas:** Automático + ajuste manual para legibilidad
- **Protección:** Desprotegida (editable por usuario)
- **Formato condicional en Sheet 2:** Colorimetría según zona de riesgo

---

## PASO 4: Checklist de Conformidad + Metadatos SGDEA

Antes de finalizar, validar:

### Checklist de Conformidad

- [ ] **Procesos identificados:** Mínimo 3 procesos por análisis.
- [ ] **Riesgos definidos:** Mínimo 1 riesgo por proceso.
- [ ] **Escala DAFP aplicada:** Probabilidad 1–5, Impacto 1–5.
- [ ] **Mapa de Calor consistente:** Zonas alineadas con matriz 5×5 oficial DAFP.
- [ ] **Controles documentados:** Cada riesgo tiene control existente descrito.
- [ ] **Tratamientos asignados:** Cada riesgo tiene tratamiento (Evitar/Reducir/Compartir/Aceptar).
- [ ] **Responsables nombrados:** Campos Q y E (Sheet 1 y 3) completos.
- [ ] **Fechas de seguimiento:** Coherentes y prospectivas.
- [ ] **Integridad de referencias:** FK consistentes entre sheets.
- [ ] **Formato visual:** Colorimetría, bordes, fuente aplicados correctamente.

### Metadatos SGDEA

Incluir en la primera fila del Sheet 1 (o hoja oculta "Metadatos"):

```
Entidad: [Nombre]
Fecha de Elaboración: [DD/MM/YYYY]
Fecha de Actualización: [DD/MM/YYYY]
Responsable del Riesgo (Área): [Nombre y cargo]
Aprobado por: [Firma / Nombre]
Versión: 1.0
Clasificación de Seguridad de la Información: [Público / Restringido / Confidencial]
Referencia Normativa: Decreto 1499/2017, Guía DAFP, Ley 1474/2011, NTC-ISO 31000:2018
```

---

## Flujo de Ejecución

1. **Recopilar datos del Paso 0** (entidad, procesos, tipos de riesgo, plantilla existente).
2. **Validar si existe PAA** y ajustar tipos de riesgo incluidos.
3. **Crear o adaptar estructura .xlsx** (4 hojas).
4. **Poblar Sheet 1** (Matriz de Riesgos) con datos del usuario o plantilla.
5. **Calcular automáticamente:**
   - Zonas inherentes (basadas en Prob. + Impacto → mapa 5×5).
   - Zonas residuales (post-control).
6. **Generar Sheet 2** (Mapa de Calor visual).
7. **Completar Sheet 3** (Plan de Tratamiento) basado en tratamientos asignados.
8. **Estructurar Sheet 4** (Seguimiento) con fechas de revisión.
9. **Aplicar formato condicional** (colorimetría).
10. **Validar Checklist de Conformidad.**
11. **Agregar metadatos SGDEA.**
12. **Guardar y entregar** archivo .xlsx.

---

## Referencias Normativas

- **Decreto 1499/2017:** Estándares de Control Interno (MIPG Dimensión 7).
- **Guía de Administración del Riesgo DAFP:** Metodología 5×5 de riesgos.
- **Ley 1474/2011:** Estatuto Anticorrupción; obligatoriedad de PAA.
- **Decreto 612/2018:** Integración de PAA en Plan Institucional.
- **NTC-ISO 31000:2018:** Principios y marco internacional de gestión de riesgos.
- **GTC-185:** Implementación de ISO 31000 en contexto colombiano.
- **Decreto 1377/2013:** Protección de datos personales (para riesgos digitales).

---

## Preguntas Frecuentes

**¿Cuál es la diferencia entre Probabilidad Inherente y Residual?**
- Inherente: riesgo sin considerar controles existentes.
- Residual: riesgo después de aplicar controles actuales.

**¿Cómo determino la escala DAFP?**
- Usa la documentación de tu entidad o la Guía DAFP oficial. Consulta con el área de riesgos.

**¿Necesito incluir riesgos de corrupción?**
- Sí, si tu entidad tiene Plan de Acción Anticorrupción (PAA) formal (Decreto 612/2018).

**¿Puedo agregar más hojas?**
- Sí. La estructura base es flexible; se pueden añadir análisis complementarios (ej: "Riesgos Estratégicos").

---

**Versión:** 1.0 | **Última actualización:** 9 de marzo de 2026 | **Contacto:** Soporte@Cowork.gov.co

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
Nivel de riesgo MPIA: Medio
Justificación del nivel: Asistencia en clasificación de riesgos institucionales. La valoración de probabilidad e impacto puede influir en decisiones de control. Requiere validación experta.
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
