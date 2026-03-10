# 🏛️ Skills de Sector Público Colombiano para Cowork

**Portafolio de 18 skills especializadas** para generar documentos institucionales del sector público colombiano en la plataforma [Cowork](https://claude.com) de Anthropic.

Cada skill guía a Claude paso a paso para producir un documento normado — oficios, planes de acción, estudios previos, informes de control interno — cumpliendo la normativa colombiana aplicable y los lineamientos de IA del Distrito (Acuerdo 003/2025 CDTD).

---

## ¿Qué hace este repositorio?

Un funcionario público abre Cowork, instala una skill, y obtiene documentos institucionales listos para revisión:

1. **Sube su plantilla** institucional (si la tiene)
2. **Responde preguntas** guiadas sobre el documento que necesita
3. **Recibe un .docx / .xlsx / .pptx** con estructura normativa, metadatos SGDEA y checklist de conformidad

No necesita saber de IA. No necesita dominar la normativa detallada. La skill ya la trae embebida.

---

## Catálogo de Skills

### Bloque 1 — Gestión Documental

| Skill | Descripción | Salida | Riesgo MPIA |
|-------|-------------|--------|-------------|
| [`oficio-memorando-entidad`](bloque-1-gestion-documental/oficio-memorando-entidad/) | Oficios, memorandos y circulares (Ley 594/2000, GTC-185) | .docx | Bajo |
| [`respuesta-pqrsdf-entidad`](bloque-1-gestion-documental/respuesta-pqrsdf-entidad/) | Respuestas a PQRSDF con control de términos legales | .docx | Medio |
| [`acta-reunion-entidad`](bloque-1-gestion-documental/acta-reunion-entidad/) | Actas de reunión con compromisos y seguimiento | .docx | Bajo |
| [`informe-gestion-entidad`](bloque-1-gestion-documental/informe-gestion-entidad/) | Informes de gestión periódicos | .docx | Bajo |

### Bloque 2 — Planeación Estratégica

| Skill | Descripción | Salida | Riesgo MPIA |
|-------|-------------|--------|-------------|
| [`plan-accion-entidad`](bloque-2-planeacion-estrategica/plan-accion-entidad/) | Plan de Acción Institucional (Decreto 612/2018, 6 hojas, 21 columnas) | .xlsx | Bajo |
| [`ficha-indicador-entidad`](bloque-2-planeacion-estrategica/ficha-indicador-entidad/) | Fichas de indicadores SMART (lote hasta 30) | .docx | Bajo |
| [`matriz-riesgos-entidad`](bloque-2-planeacion-estrategica/matriz-riesgos-entidad/) | Matriz de riesgos metodología DAFP 5×5 | .xlsx | Medio |
| [`mga-proyecto-inversion`](bloque-2-planeacion-estrategica/mga-proyecto-inversion/) | Fichas MGA para proyectos de inversión (4 módulos) | .docx | Medio |

### Bloque 3 — Contratación y Supervisión

| Skill | Descripción | Salida | Riesgo MPIA |
|-------|-------------|--------|-------------|
| [`estudios-previos-entidad`](bloque-3-contratacion-supervision/estudios-previos-entidad/) | Estudios previos (Decreto 1082/2015, 9 secciones) | .docx | Alto |
| [`informe-supervision-entidad`](bloque-3-contratacion-supervision/informe-supervision-entidad/) | Informes de supervisión contractual (Ley 1474/2011) | .docx | Medio |
| [`concepto-tecnico-entidad`](bloque-3-contratacion-supervision/concepto-tecnico-entidad/) | Conceptos técnicos institucionales (4 tipologías) | .docx | Medio |

### Bloque 4 — Transparencia y Control

| Skill | Descripción | Salida | Riesgo MPIA |
|-------|-------------|--------|-------------|
| [`paac-entidad`](bloque-4-transparencia-control/paac-entidad/) | Plan Anticorrupción y Atención al Ciudadano (Ley 1474/2011 Art. 73) | .xlsx | Bajo |
| [`rendicion-cuentas-entidad`](bloque-4-transparencia-control/rendicion-cuentas-entidad/) | Informes de rendición de cuentas (CONPES 3654/2010) | .docx | Bajo |
| [`informe-control-interno-entidad`](bloque-4-transparencia-control/informe-control-interno-entidad/) | Informes de control interno y auditoría (Ley 87/1993) | .docx | Medio |

### Bloque 5 — Comunicación Institucional

| Skill | Descripción | Salida | Riesgo MPIA |
|-------|-------------|--------|-------------|
| [`presentacion-institucional-entidad`](bloque-5-comunicacion-institucional/presentacion-institucional-entidad/) | Presentaciones .pptx por audiencia (5 modos) | .pptx | Bajo |
| [`manual-procedimientos-entidad`](bloque-5-comunicacion-institucional/manual-procedimientos-entidad/) | Manuales de procedimientos estructura DAFP | .docx | Bajo |
| [`carta-compromiso-entidad`](bloque-5-comunicacion-institucional/carta-compromiso-entidad/) | MOU, cartas de intención, acuerdos marco | .docx | Bajo |

### Transversal — Conformidad IA

| Skill | Descripción | Salida | Función |
|-------|-------------|--------|---------|
| [`conformidad-mpia-bogota`](transversal-conformidad-ia/conformidad-mpia-bogota/) | Diagnóstico MPIA-Bogotá con cálculo ICM | .docx | Dictamen de conformidad |

---

## Conformidad MPIA-Bogotá (Acuerdo 003/2025 CDTD)

Todas las skills incorporan un **bloque transversal de conformidad** con los lineamientos técnicos y éticos de IA del Distrito Capital:

- **Aviso de uso de IA** en el pie de cada documento generado
- **Metadatos de trazabilidad** para el SGDEA (herramienta, prompt, fecha, revisión humana)
- **Checklist de 7 puntos** de conformidad MPIA por documento
- **Clasificación de riesgo** específica por skill (Bajo / Medio / Alto)

La skill `conformidad-mpia-bogota` permite además generar un dictamen completo del proyecto de IA: cálculo del Índice Compuesto de Madurez (ICM = 0.40×IGD + 0.60×PDP), asignación de ruta de madurez y plan de acción para el sello de conformidad.

> Ver [`transversal-conformidad-ia/bloque_transversal_mpia.md`](transversal-conformidad-ia/bloque_transversal_mpia.md) para el detalle del bloque inyectado en cada skill.

---

## Instalación

### Opción 1: Instalar una skill individual

1. Descarga la carpeta de la skill que necesitas (ejemplo: `oficio-memorando-entidad/`)
2. Comprime la carpeta como archivo `.skill` (es un `.zip` renombrado)
3. En Cowork, arrastra el archivo `.skill` a la conversación
4. La skill queda instalada y lista para usar

### Opción 2: Usar directamente en Cowork

1. Copia el contenido del archivo `SKILL.md` de la skill que necesitas
2. En Cowork, ve a Configuración → Skills → Crear nueva skill
3. Pega el contenido y guarda
4. La skill estará disponible en tus conversaciones

### Opción 3: Descargar releases empaquetados

En la sección [Releases](../../releases) encontrarás archivos `.skill` pre-empaquetados listos para instalar.

---

## Estructura del repositorio

```
cowork-skills-sector-publico-colombia/
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── CHANGELOG.md
├── skills.json                              ← Catálogo máquina-legible
├── .gitignore
│
├── bloque-1-gestion-documental/
│   ├── README.md
│   ├── oficio-memorando-entidad/
│   │   ├── SKILL.md                         ← La skill (instrucciones para Claude)
│   │   └── references/                      ← Normativa de soporte
│   │       ├── normativa.md
│   │       └── normativa_acuerdo003_2025.md
│   ├── respuesta-pqrsdf-entidad/
│   ├── acta-reunion-entidad/
│   └── informe-gestion-entidad/
│
├── bloque-2-planeacion-estrategica/
│   ├── README.md
│   └── ... (4 skills)
│
├── bloque-3-contratacion-supervision/
│   ├── README.md
│   └── ... (3 skills)
│
├── bloque-4-transparencia-control/
│   ├── README.md
│   └── ... (3 skills)
│
├── bloque-5-comunicacion-institucional/
│   ├── README.md
│   └── ... (3 skills)
│
├── transversal-conformidad-ia/
│   ├── bloque_transversal_mpia.md           ← Template del bloque inyectado
│   └── conformidad-mpia-bogota/             ← Skill de diagnóstico
│
└── docs/
    └── guia-conformidad-mpia.md             ← Guía para TICs y directores
```

---

## Marco normativo cubierto

Este portafolio referencia y aplica, entre otras, las siguientes normas:

| Norma | Tema |
|-------|------|
| Ley 594/2000 | Ley General de Archivos |
| Acuerdo AGN 060/2001 | Gestión documental |
| GTC-185 | Norma técnica de documentación organizacional |
| Decreto 1499/2017 | MIPG — 7 dimensiones, 17 políticas |
| Decreto 612/2018 | Planes institucionales integrados |
| Ley 1474/2011 | Estatuto Anticorrupción (Arts. 73, 76, 83-85) |
| Ley 1712/2014 | Transparencia y acceso a información |
| Decreto 1082/2015 | Contratación pública — estudios previos |
| Ley 80/1993 | Estatuto General de Contratación |
| Ley 1150/2007 | Reforma de contratación pública |
| CONPES 3654/2010 | Política de rendición de cuentas |
| Ley 87/1993 | Control interno |
| Decreto 648/2017 | Jefes de control interno |
| Ley 489/1998 | Convenios interadministrativos |
| Decreto 767/2022 | Gobierno Digital |
| Acuerdo 003/2025 CDTD | Lineamientos IA Distrito Capital |

---

## Requisitos

- **Plataforma:** [Cowork](https://claude.com) de Anthropic (disponible desde marzo 2026)
- **Modelo recomendado:** Claude Sonnet 4.6 o superior
- **Sin dependencias externas:** Las skills son archivos `.md` autocontenidos con sus referencias normativas

---

## Autor

**Juan Camilo Pérez Cuervo**
- LinkedIn: [juancperez](https://www.linkedin.com/in/juancperez/)
- GitHub: [juancperez](https://github.com/juancperez)

Profesional en IA aplicada al sector público colombiano. Coordinador de Cooperación Internacional en la UAECOB (Cuerpo de Bomberos de Bogotá). Constructor de sistemas de IA institucional con cumplimiento normativo.

---

## Licencia

Este proyecto está licenciado bajo la [Licencia MIT](LICENSE).

Las normas colombianas referenciadas son de dominio público. Las skills son obras originales del autor.

---

## Contribuir

Ver [CONTRIBUTING.md](CONTRIBUTING.md) para la guía de contribución.

Se aceptan PRs para: nuevas skills de sector público, correcciones normativas, mejoras de prompts, traducciones, y reportes de issues.
