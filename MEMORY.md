# MEMORY.md - Long-Term Memory

## Model Selection Strategy (Jose's Preference)

**Default:** Use Haiku (latest) for all routine work, heartbeats, and simple tasks. Minimal cost, fast, good enough for most things.

**Sonnet:** Use for moderately complex tasks — research, multi-step analysis, document writing, moderately complex coding.

**Opus:** Use only for truly complex work — sophisticated problem-solving, heavy reasoning, complex code architecture, advanced analysis.

**Key rule:** If it's simple, Haiku wins. Don't overthink it.

---

## Profile

- **Timezone:** WIB (UTC+7) — Indonesia (Sorong, Bali)
- **Location:** Currently in Raja Ampat, Sorong; moving to Denpasar, Bali tomorrow
- **GitHub:** sparda2 (https://github.com/sparda2)

## Important Preferences

**Gateway Restart:** Automatically restart the gateway after any of these changes:
- MEMORY.md updates
- Config file modifications
- New skill creation/updates
- Any config-related changes
(2026-02-12)

---

## Página Cloning Skill (NEW - 2026-02-12)

**Objetivo:** Clonar páginas web completas para reutilizarlas en constructores (WordPress, GoHighLevel) como HTML independiente.

**Proceso estandarizado:**

1. **Descargar HTML y JavaScript**
   - `curl -s "URL" | head -200` para ver estructura
   - `curl -s "URL/ruta/script.js"` para obtener archivos JS ocultos

2. **Analizar estructura**
   - Identificar secciones principales (video, CTA, footer, etc.)
   - Mantener toda lógica de JavaScript (aunque esté ofuscada)
   - Notar qué recursos apuntan a servidores externos

3. **Crear HTML independiente**
   - CSS **inline** en `<style>` (no archivos externos)
   - Mantener toda la estructura visual idéntica
   - Imágenes/videos siguen apuntando al dominio original
   - JavaScript ofuscado incluido tal cual

4. **Optimizar para mobile & performance**
   - Responsive design (media queries)
   - Preload de recursos críticos
   - Lazy loading de imágenes (`loading="lazy"`)
   - Fonts con async + print media trick

5. **Estructura de carpetas**
   ```
   cursos_modelados/
   └── [nombre_curso]/
       ├── index.html              (ARCHIVO PRINCIPAL A USAR)
       ├── README.md               (Documentación completa)
       └── INSTRUCCIONES_RAPIDAS.md (Guía de instalación)
   ```

6. **Documentación obligatoria**
   - README con características técnicas y uso
   - INSTRUCCIONES_RAPIDAS con pasos para WordPress/GHL
   - Guía de personalización (cambiar links, imágenes, textos)

7. **Testing**
   - Verificar que HTML se abre en navegador
   - Probar en mobile (responsive)
   - Confirmar que animaciones/lógica funciona

**Feedback iterativo:**
- Jose proporcionará mejoras, cambios o feedback
- Ajustaré el skill constantemente
- Cada nueva versión mejorará sobre la anterior
- Documentaré cambios en este archivo

**Proyecto base:** `/home/juanpa-va-1/.openclaw/workspace/cursos_modelados/`

**Skill creado:** `/home/juanpa-va-1/.openclaw/workspace/skills/page-cloner/`
- SKILL.md - Instrucciones completas
- WORKFLOW.md - Paso a paso detallado
- template-page.html - Template reutilizable

**Status:** ✅ Primer proyecto completado (La Onda Zen), Skill listo, mejoras pendientes
