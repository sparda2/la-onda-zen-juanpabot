# VSL v1 - Dra. Isabel Martínez (La Onda Tranquila)

## Descripción

Página de video de ventas clonada desde `https://www.draisabelmartinez.site/ondavid18l1`

**Características:**
- Video player integrado (ConvertAI/Vturb)
- Botones de CTA animados (pulsing + zooming)
- Responsive design (mobile + desktop)
- Footer con copyright y enlaces legales
- Google Fonts (Roboto, Montserrat) con preload
- Meta tags y Open Graph configurados
- Pixel de Facebook integrado

## Estructura

```
index.html      - Página principal (todo-en-uno)
README.md       - Este archivo
```

## Instalación

### Opción 1: Servidor Local
```bash
cd vsl-v1/
python -m http.server 8000
# Abre http://localhost:8000
```

### Opción 2: WordPress
1. Crea una página en blanco
2. Cambia a "Código" (HTML)
3. Copia y pega todo el contenido de `index.html`
4. Publica

### Opción 3: GoHighLevel / Constructores
1. Abre un lienzo en blanco
2. Busca el widget "Código HTML"
3. Pega el contenido de `index.html`
4. Guarda

## Personalización

### Cambiar botones (links de compra)
Busca:
```
https://pay.hotmart.com/H102591687A?checkoutMode=10&hidebillet=1&src=VID18l1
```

Reemplaza por tu enlace de Hotmart/Stripe/etc.

### Cambiar imágenes
Las imágenes apuntan a:
```
https://media.atomicatpages.net/u/wGdxtageg6ehx6YIDoo8fZ0DIMa2/Pictures/[IMAGEN]
```

Si quieres tus propias imágenes, descárgalas y reemplaza las URLs.

### Cambiar video
El video viene de ConvertAI:
```
vturb-smartplayer id="vid-6902b577a83e5df956e6a433"
```

Para cambiar el video, necesitarás:
1. Tu propio proyecto en ConvertAI
2. Reemplazar el ID del player
3. Reemplazar la URL del stream

### Cambiar colores
- Botones verdes: `#00be00` → cambia a tu color
- Headline azul: `#033459` → tu color
- Busca y reemplaza en la sección `<style>`

## Testing

- ✅ Abre en navegador (Chrome, Firefox, Safari)
- ✅ Prueba en mobile (responsive)
- ✅ Verifica que botones redirigen correctamente
- ✅ Confirma que video carga
- ✅ Revisa animaciones (pulsing, zooming)

## Notas técnicas

- **CSS inline:** Todo en el `<head>` para máxima compatibilidad
- **JS externo:** Facebook pixel + scripts de ConvertAI
- **Imágenes con lazy loading:** `loading="lazy"` para performance
- **Fonts asincrónicas:** Google Fonts con `onload` trick
- **Sin dependencias:** No necesita jQuery, Bootstrap, etc.

---

Generado: 2026-02-12
Clonado desde: https://www.draisabelmartinez.site/ondavid18l1
