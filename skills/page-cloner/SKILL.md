# Page Cloner Skill 🧭

Clone complete web pages into independent, WordPress/GoHighLevel-ready HTML files.

## When to Use This Skill

Use this skill when Jose asks you to:
- Clone a page from a URL
- Create a WordPress/GHL-compatible HTML file
- Replicate page functionality in a single HTML file
- Convert a web page into an embeddable element

## The Process

### 1. Download & Extract

```bash
curl -s "URL" | head -200        # See HTML structure
curl -s "URL/path/to/script.js"  # Get any hidden JS files
```

Look for:
- Main structure and sections
- External JS files (especially obfuscated)
- CSS (inline vs external)
- Images and video embeds

### 2. Analyze

**Question checklist:**
- Are there hidden/obfuscated JS? → Keep it as-is
- What are the main sections? → Video? CTA buttons? Footer?
- Where do images/videos point? → Keep original URLs
- Any special animations or logic? → Document them

### 3. Create HTML File

**Rules:**
- ✅ CSS inline only (inside `<style>` tags)
- ✅ Keep ALL JavaScript exactly as-is (including obfuscated code)
- ✅ Images/videos point to original domains
- ✅ No external dependencies except CDNs
- ✅ Single file = entire page

**Structure template:**

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Your Title</title>
    
    <!-- Preconnections for performance -->
    <link rel="preconnect" href="...">
    <link rel="dns-prefetch" href="...">
    
    <!-- Fonts with async loading -->
    <link href="fonts..." media="print" onload="...">
    
    <!-- Preload critical resources -->
    <link rel="preload" href="...">
    
    <style>
        /* ALL CSS HERE - inline, no external files */
        html { ... }
        body { ... }
        /* Media queries for responsive */
        @media (max-width: 640px) { ... }
    </style>
</head>
<body>
    <!-- HTML Structure -->
    
    <!-- Scripts at end -->
    <script src="..."></script>
    <script>
        /* Your JS code here - keep obfuscated JS as-is */
    </script>
</body>
</html>
```

### 4. Optimize for Mobile & Performance

**Responsive design:**
- Base styles for mobile
- `@media (min-width: 640px)` for tablet
- `@media (min-width: 1200px)` for desktop

**Performance tricks:**
- Preload critical CSS/JS
- Lazy load images: `loading="lazy"`
- Async fonts: `media="print" onload="..."`
- DNS prefetch for external domains
- Inline critical CSS

**Mobile optimization:**
- Touch-friendly button sizes
- Proper viewport meta tag
- Test on actual phones (or mobile browser dev tools)

### 5. Create Documentation

**File 1: README.md**
- What's included (sections, features)
- Technical specs (size, performance, compatibility)
- How to use (WordPress, GoHighLevel)
- Customization guide (change links, images, texts)
- Browser compatibility

**File 2: INSTRUCCIONES_RAPIDAS.md**
- Step-by-step for WordPress
- Step-by-step for GoHighLevel
- Common changes (links, images, video IDs)
- Troubleshooting tips

### 6. Folder Structure

```
cursos_modelados/
└── [course-name]/
    ├── index.html              ← USE THIS FILE
    ├── README.md               ← Full docs
    ├── INSTRUCCIONES_RAPIDAS.md ← Quick start
    └── [PROYECTO.md]           ← Project overview (top level)
```

## Example Workflow

```
User: Clone https://example.com/sales-page

1. Download page
   curl -s "https://example.com/sales-page" | head -200

2. Find JS files
   curl -s "https://example.com/sales-page/js/hidden.js"

3. Analyze structure
   - Hero video section
   - CTA buttons with animations
   - Testimonials section
   - Footer

4. Create index.html with:
   - All HTML structure
   - CSS inline
   - JS code (obfuscated or not)
   - Images → original URLs
   - Videos → original URLs

5. Optimize
   - Add responsive media queries
   - Add preload/prefetch
   - Add lazy loading
   - Test on mobile

6. Document
   - Write README.md
   - Write INSTRUCCIONES_RAPIDAS.md
   - Create folder: cursos_modelados/[name]/

7. Done! HTML ready for WordPress/GHL
```

## Important Rules

1. **Never modify JavaScript logic** - Keep obfuscated code exactly as-is
2. **Always keep original URLs** - Images/videos point to original domains
3. **CSS must be inline** - No external stylesheets
4. **One file only** - Everything in index.html
5. **Mobile first** - Design responsive from the start

## Customization Guide (for users)

Tell users they can easily change:
- **Links:** Search for full URLs, replace all instances
- **Images:** Find `<img src="...">`, update URL
- **Video IDs:** Search for unique video ID, replace
- **Texts:** Find text in HTML, change directly
- **Colors:** Find hex colors in `<style>`, edit

## Performance Checklist

- [ ] CSS is inline (no external .css files)
- [ ] Images have `loading="lazy"`
- [ ] Critical resources are preloaded
- [ ] Fonts load asynchronously
- [ ] File size is reasonable (<50KB for simple pages)
- [ ] Mobile responsiveness tested
- [ ] All animations work smoothly

## Feedback Loop

After creating the page:
1. Test in browser (desktop + mobile)
2. Ask Jose for feedback
3. Document any issues he finds
4. Update the skill with improvements
5. Apply changes to future clones

## Resources

- Base directory: `/home/juanpa-va-1/.openclaw/workspace/cursos_modelados/`
- Memory notes: Check MEMORY.md for updates
- Previous examples: Check `la_onda_zen/` folder

---

**This skill is iterative.** Jose will provide feedback, and you'll improve it each time. Document all changes in MEMORY.md.
