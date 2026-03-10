# Transversal — Conformidad IA (MPIA-Bogotá)

Sistema de conformidad con los lineamientos técnicos y éticos de IA del Distrito Capital (Acuerdo 003/2025 CDTD).

## Arquitectura de dos capas

### Capa 1: Bloque transversal (por documento)

Cada una de las 17 skills de generación de documentos incluye un **bloque de conformidad MPIA** al final, que instruye a Claude para:

1. **Insertar aviso de uso de IA** en el pie de cada documento generado
2. **Generar metadatos de trazabilidad** para el SGDEA (herramienta, modelo, fecha, prompt resumido, revisión humana)
3. **Ejecutar checklist de 7 puntos** de conformidad antes de entregar el documento
4. **Clasificar el riesgo** del documento según la tabla de riesgo MPIA

Ver [`bloque_transversal_mpia.md`](bloque_transversal_mpia.md) para el template del bloque.

### Capa 2: Skill de diagnóstico (por proyecto)

La skill `conformidad-mpia-bogota` es una herramienta para TICs y directores de entidades distritales que permite evaluar el nivel de madurez de un proyecto de IA frente al MPIA-Bogotá.

Genera un dictamen .docx con:

- **Ficha técnica** del proyecto de IA evaluado
- **Diagnóstico IGD** (Índice de Gobierno Digital) — 11 subíndices
- **Cálculo PDP** (Puntaje por Determinantes del Proyecto) — 8 factores ponderados
- **ICM** (Índice Compuesto de Madurez) = 0.40 × IGD + 0.60 × PDP
- **Ruta de madurez**: Exploratoria (0-39), Consolidación (40-69), Avanzada (70-100)
- **Clasificación de riesgo** de cada sistema de IA (Bajo/Medio/Alto/Crítico)
- **Checklist Fase 1** (obligatoria) y **Fase 2** (según ruta)
- **Plan de acción** con actividades, responsables y plazos
- **Dictamen final** con concepto de conformidad

## Clasificación de riesgo por skill

| Skill | Riesgo | Justificación |
|-------|--------|---------------|
| oficio-memorando-entidad | Bajo | Documento informativo |
| respuesta-pqrsdf-entidad | Medio | Interacción con ciudadanos, plazos legales |
| acta-reunion-entidad | Bajo | Registro interno |
| informe-gestion-entidad | Bajo | Documento informativo |
| plan-accion-entidad | Bajo | Instrumento de planeación |
| ficha-indicador-entidad | Bajo | Instrumento técnico |
| matriz-riesgos-entidad | Medio | Influye en controles institucionales |
| mga-proyecto-inversion | Medio | Asignación de recursos |
| estudios-previos-entidad | **Alto** | Influencia directa en contratación pública |
| informe-supervision-entidad | Medio | Seguimiento contractual |
| concepto-tecnico-entidad | Medio | Puede influir en decisiones |
| paac-entidad | Bajo | Instrumento de planeación |
| rendicion-cuentas-entidad | Bajo | Documento informativo |
| informe-control-interno-entidad | Medio | Puede generar hallazgos |
| presentacion-institucional-entidad | Bajo | Material visual |
| manual-procedimientos-entidad | Bajo | Documentación interna |
| carta-compromiso-entidad | Bajo | Sin obligaciones financieras |

## Normativa

- **Acuerdo 003/2025 CDTD** — Lineamientos técnicos y éticos para el uso de IA en entidades distritales de Bogotá
- Emitido por la Comisión Distrital de Transformación Digital, 26 de diciembre de 2025
