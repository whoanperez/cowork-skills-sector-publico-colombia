# Guía de Contribución

Gracias por tu interés en contribuir a las Skills de Sector Público Colombiano para Cowork.

## ¿Cómo contribuir?

### Reportar un problema

Si encontraste un error normativo, un problema en la generación de documentos, o una mejora posible, abre un [Issue](../../issues) con:

- **Skill afectada** (nombre exacto, ej: `oficio-memorando-entidad`)
- **Descripción del problema** (qué pasa vs. qué debería pasar)
- **Referencia normativa** (si aplica, cita la norma, artículo y año)

### Proponer una nueva skill

1. Abre un Issue con la etiqueta `nueva-skill` describiendo:
   - Qué documento genera
   - Qué entidades lo necesitan
   - Normativa aplicable (leyes, decretos, resoluciones)
   - Formato de salida (.docx, .xlsx, .pptx)

2. Si quieres desarrollarla tú mismo, sigue la estructura descrita abajo.

### Enviar un Pull Request

1. Haz fork del repositorio
2. Crea una rama: `git checkout -b feature/nombre-de-la-skill`
3. Sigue la estructura estándar (ver abajo)
4. Asegúrate de que la skill incluya el bloque transversal MPIA
5. Envía tu PR con una descripción clara

---

## Estructura estándar de una skill

Cada skill debe seguir esta estructura de archivos:

```
nombre-de-la-skill/
├── SKILL.md              ← Instrucciones para Claude (obligatorio)
└── references/           ← Normativa de soporte (obligatorio)
    ├── normativa_xxx.md  ← Extracto de las normas aplicables
    └── normativa_acuerdo003_2025.md  ← Referencia MPIA (obligatorio)
```

### Formato del SKILL.md

```yaml
---
name: nombre-en-kebab-case
description: >
  Descripción clara de qué genera la skill, qué normativa aplica,
  y los triggers de activación (palabras clave que la invocan).
---
```

El cuerpo del SKILL.md debe incluir, en orden:

1. **Título y contexto** — Qué documento genera y para quién
2. **Referencia normativa** — Link al archivo en `references/`
3. **Paso 0: Recolección** — Preguntas para obtener información del usuario
4. **Pasos 1+: Generación** — Instrucciones de estructura y contenido del documento
5. **Checklist de conformidad** — Verificación normativa antes de entregar
6. **Metadatos SGDEA** — Campos de radicación y trazabilidad
7. **Marco normativo** — Lista de normas aplicadas
8. **Notas de uso** — Advertencias y limitaciones
9. **Bloque MPIA** — Conformidad Acuerdo 003/2025 (ver `transversal-conformidad-ia/bloque_transversal_mpia.md`)

### Clasificación de riesgo MPIA

Toda skill nueva debe incluir una clasificación de riesgo según el Acuerdo 003/2025 CDTD:

| Nivel | Criterio |
|-------|----------|
| **Bajo** | Documentos informativos, presentaciones, manuales internos |
| **Medio** | Documentos con implicaciones legales parciales, interacción ciudadana |
| **Alto** | Documentos que influyen en asignación de recursos públicos |
| **Crítico** | No aplica — skills que generarían actos administrativos vinculantes están excluidas por diseño |

---

## Restricciones por diseño

Este portafolio **no incluye** y **no aceptará** skills que:

- Generen actos administrativos (resoluciones, decretos, acuerdos)
- Produzcan conceptos jurídicos vinculantes
- Tomen decisiones autónomas sin supervisión humana
- Procesen datos personales sensibles sin controles adicionales

Esto es por cumplimiento del Acuerdo 003/2025 CDTD, Sección 10 (Uso Cotidiano de IA).

---

## Convenciones de código

- **Nombres de skills:** `kebab-case` terminando en `-entidad` (para skills genéricas de sector público)
- **Idioma:** Español colombiano (sin regionalismos excesivos)
- **Referencias normativas:** Siempre citar Ley/Decreto/Resolución + número + año + artículos específicos
- **Líneas:** Máximo ~800 líneas por SKILL.md (si excede, dividir en sub-skills)

---

## Código de conducta

Nos adherimos al [Código de Conducta del Pacto de Contribuyentes](https://www.contributor-covenant.org/version/2/1/code_of_conduct/). Tratamos a todos con respeto y profesionalismo.

## Licencia

Al contribuir, aceptas que tus contribuciones se licenciarán bajo la [Licencia MIT](LICENSE) del proyecto.
