# Page Cloner Workflow - Paso a Paso

Esta es la guía exacta que sigo cuando Jose me pide clonar una página.

## Fase 1: Investigación (5 min)

### Paso 1a: Descargar HTML base
```bash
curl -s "https://example.com/page" > page.html
head -500 page.html  # Ver estructura
```

**Busca:**
- Estructura HTML (secciones, divs, ids)
- Referencias a scripts externos
- Links a CSS externo
- Imágenes y videos
- Meta tags importantes

### Paso 1b: Encontrar y descargar JavaScript oculto
```bash
curl -s "https://example.com/js/hidden.js"
curl -s "https://example.com/ondavid18l2/js/zyWawY7693486.js"
```

**Nota:** Busca patrones como:
- `<script src="...">` en el HTML
- Rutas en archivos CSS
- Referencias en meta tags

### Paso 1c: Identificar secciones principales
Del HTML extraído, lista:
- **Hero/Header** - Video, imágenes grandes
- **CTA Sections** - Botones, llamadas a acción
- **Content** - Textos, formularios
- **Footer** - Links, copyright
- **Scripts** - Lógica, tracking, pixel

## Fase 2: Creación del HTML (15 min)

### Paso 2a: Estructura base
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Tu Título</title>
    
    <!-- Fonts, preload, prefetch -->
    ...
    
    <style>
        /* TODO el CSS aquí - INLINE */
    </style>
</head>
<body>
    <!-- TODO el HTML aquí -->
    
    <!-- Scripts al final -->
</body>
</html>
```

### Paso 2b: Copiar HTML del original
- Extrae secciones del HTML descargado
- Simplifica IDs y clases si es necesario
- Mantén la estructura visual idéntica

### Paso 2c: Copiar CSS del original
- Si está en `<style>` tags → copia completo
- Si está en archivos `.css` → descargar y copiar inline
- Mantén media queries (responsive)

### Paso 2d: Copiar JavaScript completo
- El código ofuscado va tal cual
- El código legible va como está
- No modifiques nada, solo copia

### Paso 2e: Optimizar para mobile
Añade media queries si faltan:
```css
@media (max-width: 640px) {
    /* Estilos para móvil */
    padding: reducido;
    font-size: más pequeño;
    max-width: ajustado;
}
```

## Fase 3: Optimización (10 min)

### Paso 3a: Performance
- Añade `loading="lazy"` a todas las imágenes
- Preload recursos críticos (videos, scripts)
- Fonts con media="print" trick para async
- DNS prefetch para dominios externos

### Paso 3b: Responsive
- Prueba en móvil (dev tools F12)
- Ajusta padding/margin en media queries
- Verifica que los botones sean clickeables
- Prueba en tablet también

### Paso 3c: Validación
- Abre en navegador → sin errores de consola
- Ve el video/contenido
- Haz clic en botones
- Prueba en mobile

## Fase 4: Documentación (10 min)

### Paso 4a: README.md
```markdown
# [Nombre del Curso]

## Características
- ✅ Item 1
- ✅ Item 2
- ✅ Video con player X
- ✅ Botones con animación Y

## Uso
### WordPress
1. Nueva página → Bloque HTML
2. Copia todo el index.html
3. Pégalo → Publica

### GoHighLevel
1. Página → Custom HTML
2. Copia todo el index.html
3. Pégalo → Guarda

## Personalización
- Botones: busca https://pay.hotmart...
- Imágenes: busca https://media...
- Video ID: busca 6933b4be...

## Técnico
- Tamaño: XXkb
- Responsive: Sí
- Mobile: Optimizado
- Performance: XXms
```

### Paso 4b: INSTRUCCIONES_RAPIDAS.md
```markdown
# 🚀 Instalación Rápida

## WordPress
1. Crea página nueva
2. Clic en + → HTML personalizado
3. Copia index.html completo
4. Pégalo
5. Publica ✅

## GoHighLevel
1. Abre tu página
2. Custom HTML
3. Copia index.html completo
4. Pégalo
5. Guarda ✅

## Cambios comunes
- Link: Busca https://pay.hotmart...
- Imagen: Busca https://media...
- Video: Busca ID-VIDEO-AQUI
```

## Fase 5: Organización (5 min)

### Paso 5a: Crear carpeta
```bash
mkdir -p cursos_modelados/[nombre-curso]
```

### Paso 5b: Mover archivos
```
cursos_modelados/
└── nombre-curso/
    ├── index.html
    ├── README.md
    └── INSTRUCCIONES_RAPIDAS.md
```

### Paso 5c: Registrar en PROYECTO.md
Añade entrada en el archivo de proyecto

## Checklist Final

- [ ] HTML válido (sin errores en consola)
- [ ] Se ve igual al original
- [ ] Responsive en móvil/tablet/desktop
- [ ] Video/contenido carga correctamente
- [ ] Botones son clickeables
- [ ] Animaciones funcionan
- [ ] Images usan lazy loading
- [ ] README.md completo
- [ ] INSTRUCCIONES_RAPIDAS.md clara
- [ ] Carpeta bien organizada

## Tiempo Total

- Fase 1 (Investigación): 5 min
- Fase 2 (HTML): 15 min
- Fase 3 (Optimización): 10 min
- Fase 4 (Documentación): 10 min
- Fase 5 (Organización): 5 min

**Total: 45 minutos por página**

## Feedback Loop

Después de cada página:
1. Jose la prueba en WordPress/GHL
2. Da feedback (qué cambiar, mejorar)
3. Yo ajusto el skill con las lecciones aprendidas
4. Próxima página sale mejor

---

**Nota:** Este workflow es base. Se mejora con cada feedback de Jose.
