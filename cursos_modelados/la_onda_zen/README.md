# La Onda Zen - HTML Independiente

Esta es una versión completamente independiente de la página de presentación de "La Onda Zen", optimizada para ser insertada en constructores como WordPress y GoHighLevel.

## 📁 Archivos

- `index.html` - Archivo HTML completo y autocontenido

## 🎯 Características

✅ **Completamente independiente** - No requiere carpetas de apoyo ni archivos externos (excepto CDN)
✅ **Optimizado para mobile** - Responsive en todos los tamaños de pantalla
✅ **Carga ultrarrápida** - CSS inline, preload de recursos críticos
✅ **Lógica oculta intacta** - Mantiene la lógica de JavaScript ofuscada del original
✅ **Imágenes y videos originales** - Apuntan al servidor original de draisabelmartinez.site
✅ **Animaciones fluidas** - Efectos pulsing y zooming del original

## 📱 Uso en WordPress

1. Crea una página nueva
2. Añade un bloque personalizado (HTML custom)
3. Copia TODO el contenido de `index.html`
4. Pégalo en el bloque
5. Publica la página

O simplemente inserta el código usando el plugin `Advanced HTML`

## 🚀 Uso en GoHighLevel (GHL)

1. Ve a tu funnel o página
2. Añade un elemento `Custom HTML`
3. Copia TODO el contenido de `index.html`
4. Pégalo en el editor de HTML
5. Guarda los cambios

## 🔧 Características técnicas

- **Responsive Design** - Se adapta a mobile, tablet y desktop
- **Performance** - Preload de recursos críticos, lazy loading de imágenes
- **SEO** - Meta tags correctos (aunque está marcado como noindex)
- **Compatibilidad** - Funciona en todos los navegadores modernos

## 📊 Estructura del HTML

```
- Encabezado (meta tags, fonts, preload)
- Video SmartPlayer (contenedor vturb)
- CTA Section (botones con animaciones)
  - Botón superior (pulsing)
  - Imágenes de beneficios
  - Botón inferior (zooming)
- Footer
- Scripts (SmartPlayer + lógica oculta + Meta Pixel)
```

## 🎨 Personalización

Si necesitas cambiar:

- **Links del botón** - Busca todas las instancias de `https://pay.hotmart.com/...` 
- **Imágenes** - Las URLs están claramente marcadas en las etiquetas `<img>`
- **Textos** - Busca y reemplaza directamente en el HTML
- **Colores** - Los estilos están en la sección `<style>`
- **ID del video** - Busca `6933b4be44e4e1560f6e1c5c`

## ⚡ Notas de rendimiento

- Las fonts de Google se cargan de forma asincrónica
- El video usa preload para DNS prefetch
- Las imágenes usan `loading="lazy"` para carga gradual
- El CSS es inline para eliminar solicitudes de archivo externo

## 🔐 Seguridad

- Meta robots está en `noindex, nofollow` (como original)
- La lógica de JavaScript es ofuscada (protegida)
- No hay datos sensibles en el HTML

## 📝 Información de contacto

Para soporte o preguntas sobre esta implementación, contacta a JuanPa. 🧭
