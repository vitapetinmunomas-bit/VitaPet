# 🚀 VITAPET INMUNO + - GUÍA DE CONFIGURACIÓN

## 📋 ÍNDICE

1. [Requisitos](#requisitos)
2. [Instalación Local](#instalación-local)
3. [Estructura del Proyecto](#estructura-del-proyecto)
4. [Descargar Imágenes](#descargar-imágenes)
5. [Verificación](#verificación)
6. [Desplegamiento](#desplegamiento)
7. [Personalizaciones](#personalizaciones)
8. [Optimización](#optimización)
9. [Troubleshooting](#troubleshooting)

---

## ✅ Requisitos

- **Git** (para versionado)
- **Navegador web moderno** (Chrome, Safari, Firefox, Edge)
- **Editor de código** (VS Code, Sublime, Atom)
- **Conexión a internet** (para descargas de imágenes)
- **Opcional:** Node.js + npm (para herramientas de construcción)

---

## 🔧 Instalación Local

### 1. Clona el repositorio

```bash
git clone https://github.com/vitapetinmunomas-bit/VitaPet.git
cd VitaPet
```

### 2. Abre en tu editor

```bash
# VS Code
code .

# Sublime Text
subl .

# Atom
atom .
```

### 3. Estructura de archivos

```
VitaPet/
├── images/                 # Imágenes (descarga aquí)
├── index.html             # Página principal
├── styles.css             # Estilos (1000+ líneas)
├── script.js              # JavaScript interactivo
├── IMAGES_GUIDE.md        # Guía de imágenes
├── SETUP_GUIDE.md         # Este archivo
├── DESIGN_SPECS.md        # Especificaciones
└── README.md              # Documentación
```

---

## 🎨 Estructura del Proyecto

### index.html
- 10 secciones estratégicas
- Semántica HTML5
- Meta tags completos
- Optimizado para SEO

### styles.css
- 1000+ líneas de CSS puro
- Glassmorphism design
- Animaciones suaves
- Responsive breakpoints
- Variables CSS (--custom-properties)

### script.js
- Smooth scroll
- Parallax effects
- Lazy loading de imágenes
- Intersection Observer
- Mobile optimizations

---

## 📸 Descargar Imágenes

### Opción 1: Script Automático (Recomendado)

#### macOS/Linux:
```bash
chmod +x download-images.sh
./download-images.sh
```

#### Windows (PowerShell):
```powershell
Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope Process
.\download-images.ps1
```

### Opción 2: Manual (Ver IMAGES_GUIDE.md)

1. Crea carpeta `images/`
2. Descarga 9 imágenes de Unsplash
3. Guarda con nombres exactos

Ver `IMAGES_GUIDE.md` para URLs y pasos detallados.

---

## ✓ Verificación

### 1. Verifica la estructura

```bash
# macOS/Linux
ls -la
tree images/

# Windows
dir
dir images
```

Deberías ver:
```
✓ index.html
✓ styles.css
✓ script.js
✓ IMAGES_GUIDE.md
✓ SETUP_GUIDE.md
✓ DESIGN_SPECS.md
✓ images/ (carpeta con 9 imágenes JPG)
```

### 2. Abre en navegador

```bash
# macOS
open index.html

# Linux
firefox index.html

# Windows
start index.html
```

O abre directamente: `Archivo → Abrir → index.html`

### 3. Verifica en consola del navegador

Presiona `F12` y busca:
- ✓ "VitaPet página cargada completamente"
- ✓ Sin errores en rojo
- ✓ Todas las imágenes cargan

---

## 🌐 Desplegamiento

### Opción 1: GitHub Pages (Gratis, Recomendado)

#### Paso 1: Push a GitHub
```bash
git add .
git commit -m "✨ VitaPet Inmuno + - Premium website v1.0"
git push origin main
```

#### Paso 2: Habilitar GitHub Pages
1. Ve a tu repositorio
2. Settings → Pages
3. Source: `main` branch
4. Save

#### Paso 3: Accede a tu sitio
```
https://vitapetinmunomas-bit.github.io/VitaPet/
```

**Espera 1-2 minutos** para que se active.

### Opción 2: Netlify (Alternativa)

1. Sube a GitHub (completar Paso 1 arriba)
2. Ve a [netlify.com](https://netlify.com)
3. Conecta tu repo
4. Deploy automático ✓

### Opción 3: Vercel (Alternativa)

1. Sube a GitHub
2. Ve a [vercel.com](https://vercel.com)
3. Importa proyecto
4. Deploy en 30 segundos ✓

---

## 🎯 Personalizaciones

### Cambiar textos

Abre `index.html` y modifica:

```html
<!-- Cambiar email -->
<a href="mailto:contacto@vitapet.cl">contacto@vitapet.cl</a>

<!-- Cambiar nombre empresa -->
<span class="logo-text">VitaPet</span>

<!-- Cambiar precio -->
Comprar Ahora - $49.990 CLP

<!-- Cambiar tagline -->
<p class="hero-subtitle">Tu propio mensaje aquí</p>
```

### Cambiar colores

Edita `styles.css` - bloque `:root`:

```css
:root {
    --dark-green: #1C2B1F;        /* Cambiar aquí */
    --natural-green: #4CAF50;     /* O aquí */
    --soft-gold: #D4AF37;         /* O aquí */
}
```

### Agregar secciones

Copia este template en `index.html`:

```html
<section class="nueva-seccion">
    <div class="container">
        <div class="section-header">
            <span class="label-section">ETIQUETA</span>
            <h2>Tu Título</h2>
            <p>Descripción breve</p>
        </div>
        <!-- Tu contenido -->
    </div>
</section>
```

### Agregar CSS

Agrega al final de `styles.css`:

```css
.nueva-seccion {
    padding: var(--spacing-2xl) var(--spacing-lg);
    background: var(--white);
}

.nueva-seccion h2 {
    color: var(--dark-green);
}
```

---

## ⚡ Optimización

### 1. Comprimir imágenes

```bash
# Usar TinyPNG.com o ImageOptim
# O usar CLI:
convert image.jpg -quality 85 image-optimized.jpg
```

### 2. Minificar CSS/JS (Opcional)

```bash
# Instalar herramientas
npm install -g terser cssnano-cli

# Minificar
terser script.js -o script.min.js
cssnano styles.css -o styles.min.css
```

Actualizar en `index.html`:
```html
<link rel="stylesheet" href="styles.min.css">
<script src="script.min.js"></script>
```

### 3. Lazy loading de imágenes

Ya implementado en `script.js`. Para habilitar:

```html
<!-- Usar data-src en lugar de src -->
<img data-src="images/image.jpg" alt="...">
```

### 4. Precarga de recursos

Agrega en `<head>` de `index.html`:

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://images.unsplash.com">
<link rel="dns-prefetch" href="//cdn.example.com">
```

### 5. Caché del navegador

Crear `.htaccess` en la raíz:

```apache
<IfModule mod_expires.c>
    ExpiresActive On
    ExpiresByType image/jpeg "access plus 1 month"
    ExpiresByType image/jpg "access plus 1 month"
    ExpiresByType text/css "access plus 1 week"
    ExpiresByType text/javascript "access plus 1 week"
</IfModule>
```

---

## 🐛 Troubleshooting

### Las imágenes no cargan

**Problema:** Ves placeholders grises
**Solución:**
1. Verifica que exista carpeta `images/`
2. Que los archivos tengan nombres EXACTOS
3. Que sean JPG/JPEG
4. Revisa Console (F12) por errores 404

```bash
# Verificar archivos
ls images/
# Deberías ver 9 archivos JPG
```

### Sitio lento

**Problema:** Tardío en cargar
**Solución:**
1. Comprimir imágenes a < 200KB cada una
2. Usar CDN para fuentes (ya hecho)
3. Minificar CSS/JS
4. Habilitar gzip en servidor

### CSS no aplicado

**Problema:** Sitio sin estilos
**Solución:**
1. Verifica ruta: `<link rel="stylesheet" href="styles.css">`
2. Hard refresh: Ctrl+Shift+R (Windows) o Cmd+Shift+R (Mac)
3. Limpia caché del navegador

### JavaScript errores

**Problema:** Animaciones no funcionan
**Solución:**
1. Abre Console (F12)
2. Lee el error
3. Verifica que `script.js` esté en raíz
4. Recarga la página

### GitHub Pages no funciona

**Problema:** Sitio no aparece en `github.io`
**Solución:**
1. Settings → Pages
2. Asegura que Source sea `main`
3. Espera 2-3 minutos
4. Hace hard refresh de la página de settings

### Rutas rotas después de desplegamiento

**Problema:** Links internos no funcionan
**Solución:**
1. Usa rutas relativas (ya está hecho)
2. No uses `/` al inicio
3. Ejemplo correcto:
   ```html
   <!-- ✓ Bien -->
   <img src="images/image.jpg">
   
   <!-- ✗ Mal -->
   <img src="/images/image.jpg">
   ```

---

## 📱 Testing Responsivo

### Dispositivos a probar:

```
Mobile:    320px (iPhone SE), 375px (iPhone), 414px (iPhone Plus)
Tablet:    768px (iPad), 1024px (iPad Pro)
Desktop:   1280px, 1440px, 1920px
```

### Usando DevTools:

1. Abre `index.html`
2. Presiona `F12`
3. Haz clic en ícono de dispositivo (esquina superior izq)
4. Selecciona dispositivos de la lista

### Checklist:

- [ ] Mobile (320px) - Todo funciona
- [ ] Tablet (768px) - Layout adaptado
- [ ] Desktop (1200px+) - Versión completa
- [ ] Scroll smooth
- [ ] Animaciones suaves
- [ ] Imágenes responsive
- [ ] Botones clickeables
- [ ] Links navegables

---

## 🔐 Seguridad

### Checklist:

- [ ] No hay datos sensibles en el código
- [ ] Links externos son HTTPS
- [ ] Formularios (futuros) validados
- [ ] No hay vulnerabilidades de XSS
- [ ] Meta tags de seguridad presentes

### Agregar headers de seguridad

Crear `_headers` en raíz (para Netlify):

```
/*
  X-Frame-Options: DENY
  X-Content-Type-Options: nosniff
  X-XSS-Protection: 1; mode=block
  Referrer-Policy: strict-origin-when-cross-origin
  Permissions-Policy: geolocation=(), camera=(), microphone=()
```

---

## 📊 Analytics (Futuro)

Agregar en `<head>` de `index.html`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

Reemplaza `G-XXXXXXXXXX` con tu ID de Google Analytics.

---

## 🎓 Próximos Pasos

### Corto Plazo (Esta semana):
- [ ] Descargar imágenes
- [ ] Verificar en local
- [ ] Publicar en GitHub Pages
- [ ] Compartir URL

### Mediano Plazo (Este mes):
- [ ] Integrar formulario de contacto
- [ ] Agregar Google Analytics
- [ ] Optimizar para SEO
- [ ] Agregar blog

### Largo Plazo (Este trimestre):
- [ ] E-commerce integration (Shopify/WooCommerce)
- [ ] Multiidioma (ES/EN)
- [ ] CMS (Contentful, Strapi)
- [ ] Expandir a otros países

---

## 📞 Soporte

### Documentos incluidos:
- `DESIGN_SPECS.md` - Especificaciones de diseño
- `IMAGES_GUIDE.md` - Guía de imágenes
- `SETUP_GUIDE.md` - Este documento

### Recursos externos:
- [MDN Web Docs](https://developer.mozilla.org)
- [CSS-Tricks](https://css-tricks.com)
- [Stackoverflow](https://stackoverflow.com)
- [GitHub Docs](https://docs.github.com)

---

## ✅ CHECKLIST FINAL

Antes de considerar el sitio "listo":

- [ ] Todas las imágenes descargas y en carpeta `images/`
- [ ] Sin errores en Console (F12)
- [ ] Responsive en mobile/tablet/desktop
- [ ] Animaciones suaves sin lag
- [ ] Todos los links funcionan
- [ ] Publicado en GitHub Pages o Netlify
- [ ] URL compartible funcionando
- [ ] Testeado en 3+ navegadores
- [ ] Performance > 3s load time
- [ ] SEO básico completado

---

**Versión:** 1.0
**Última actualización:** Marzo 2026
**Status:** ✅ Listo para producción
**Autor:** VitaPet Development Team

¿Preguntas? Abre un issue en GitHub o contacta a contacto@vitapet.cl
