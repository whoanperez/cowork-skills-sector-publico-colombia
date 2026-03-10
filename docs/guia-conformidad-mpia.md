# Guía de Conformidad MPIA-Bogotá para Skills de Cowork

**Audiencia:** TICs (jefes de tecnología) y directores de entidades distritales de Bogotá.

**Propósito:** Explicar cómo las skills de este portafolio cumplen con el Acuerdo 003/2025 CDTD y cómo avanzar hacia el sello de conformidad MPIA-Bogotá.

---

## ¿Qué es el MPIA-Bogotá?

El Modelo de Preparación e Implementación del Lineamiento Distrital de IA (MPIA-Bogotá) es el marco creado por la Comisión Distrital de Transformación Digital mediante el Acuerdo 003 del 26 de diciembre de 2025. Establece las reglas para que las entidades distritales de Bogotá adopten herramientas de IA de forma ética, segura y trazable.

El modelo se estructura en un ciclo PHVA (Planear-Hacer-Verificar-Actuar) con 3 fases:

- **Fase 1 (obligatoria):** Evaluación inicial — toda entidad que use IA debe cumplirla
- **Fase 2:** Implementación según ruta de madurez
- **Fase 3:** Mejora continua y reporte

## ¿Cómo se mide la madurez?

El Acuerdo define el Índice Compuesto de Madurez (ICM):

```
ICM = 0.40 × IGD + 0.60 × PDP
```

Donde:
- **IGD** = Índice de Gobierno Digital (medido por MinTIC, 11 subíndices)
- **PDP** = Puntaje por Determinantes del Proyecto (8 factores ponderados por la entidad)

Los 8 factores del PDP son:

| Factor | Peso |
|--------|------|
| Alineación con PETI | 10% |
| Recursos disponibles | 15% |
| Alcance y complejidad | 10% |
| Sostenibilidad | 15% |
| Capacidad de ejecución | 10% |
| ICC/SE (impacto ciudadano) | 20% |
| Manuales y protocolos | 10% |
| Datos personales | 10% |

El ICM determina la ruta de madurez:

| Rango ICM | Ruta | Significado |
|-----------|------|-------------|
| 0–39 | Exploratoria | La entidad está comenzando, requiere pilotos controlados |
| 40–69 | Consolidación | La entidad tiene capacidades parciales, puede escalar con controles |
| 70–100 | Avanzada | La entidad tiene madurez para implementaciones complejas |

## ¿Cómo clasifican las skills en este marco?

Las skills de este portafolio se clasifican como **categoría (g): IA Generativa** según la taxonomía del Acuerdo (Sección 7). Esto significa que son herramientas de generación de contenido textual asistido por IA.

La Sección 10 del Acuerdo regula el "Uso Cotidiano de IA" y establece que:

- **Se permite:** Usar IA como asistente para redacción, análisis y generación de borradores
- **Se exige:** Supervisión humana obligatoria, etiquetado del documento, trazabilidad
- **Se prohíbe:** Generar actos administrativos, conceptos jurídicos vinculantes, o tomar decisiones autónomas

Las skills cumplen con esto por diseño:

1. Generan **borradores** que requieren revisión humana antes de su uso oficial
2. Incluyen **aviso de uso de IA** en el documento
3. Registran **metadatos de trazabilidad** para el SGDEA
4. No generan actos administrativos ni documentos vinculantes
5. Clasifican su **nivel de riesgo** (Bajo/Medio/Alto) por documento

## ¿Qué debe hacer la entidad?

### Si solo usa las skills como herramientas de productividad

Cumplir con la Fase 1 (obligatoria):

1. Notificar a la oficina TIC que se están usando herramientas de IA generativa
2. Registrar las skills en el inventario de herramientas de IA de la entidad
3. Asegurar que los funcionarios revisan cada documento antes de firmarlo
4. Conservar los metadatos de trazabilidad en el SGDEA
5. Clasificar el uso según el nivel de riesgo

### Si quiere avanzar hacia el sello de conformidad

Usar la skill `conformidad-mpia-bogota` para:

1. Generar el diagnóstico ICM de la entidad
2. Identificar su ruta de madurez
3. Obtener el checklist Fase 2 específico para su ruta
4. Crear un plan de acción con responsables y plazos
5. Documentar el avance para reportar a la Comisión Distrital de Transformación Digital

## Restricciones de diseño del portafolio

Este portafolio excluye deliberadamente cualquier skill que:

- Genere resoluciones, decretos u otros actos administrativos
- Produzca conceptos jurídicos vinculantes
- Tome decisiones sin intervención humana
- Procese datos personales sensibles sin controles adicionales
- Interactúe directamente con ciudadanos sin supervisión

Estas restricciones existen para cumplir con la Sección 10 del Acuerdo 003/2025 y para mantener la clasificación de riesgo del portafolio dentro de niveles manejables (Bajo a Alto, nunca Crítico).
