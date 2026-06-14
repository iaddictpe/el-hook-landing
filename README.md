# El Hook · by iAddict — Landing

Landing page de **El Hook**, el servicio de contenido por suscripción de iAddict: carruseles, reels, captions y avatares en IA listos para publicar cada mes.

🔗 **Producción:** https://el-hook-landing.vercel.app

## Stack

Sitio estático — **un solo `index.html`** con CSS y JS inline. Sin build, sin dependencias. Despliegue instantáneo en Vercel.

## Estructura

```
.
├── index.html            # Landing completa (HTML + CSS + JS)
├── vercel.json           # Headers de seguridad, caché y clean URLs
├── robots.txt · sitemap.xml · site.webmanifest
├── favicon-16/32.png · apple-touch-icon.png
├── og/og-image.jpg       # Imagen de preview social (1200×630)
├── marca/                # Logo e iconos de marca (SVG)
├── ejemplos/             # Carruseles de muestra
├── realismo/             # Avatares IA (detalle) — WebP
├── photoshoot/           # Photoshoot de producto — WebP
└── videos/higgsfield/    # Reels UGC (MP4) + productos
```

## Trabajo de profesionalización

Partiendo del HTML original, se elevó a estándar de producción:

- **Performance:** assets optimizados de **53 MB → ~10 MB**. PNGs de 1856 px convertidos a WebP a resolución de display.
- **Tipografía:** carga real de Inter (antes declarada pero nunca cargada) + Playfair Display para los acentos serif.
- **Sistema de diseño:** tokens de espaciado (8 pt), sombras por capas, escala de radios, ritmo vertical consistente.
- **Responsive:** tipografía fluida con `clamp()`, breakpoints en 1024/820/720/560/420 px, tap targets ≥ 44 px, cero overflow horizontal.
- **Motion:** scroll-reveal con `IntersectionObserver`, sombra de nav al hacer scroll, respeto total a `prefers-reduced-motion`.
- **Accesibilidad:** skip-link, `:focus-visible`, landmarks semánticos (`main`, `header`, `footer`), `aria-label`s.
- **SEO:** meta description, canonical, Open Graph + Twitter Cards, imagen OG, `theme-color`.
- **Datos estructurados:** JSON-LD `Organization`, `Service` (con ofertas y precios) y `FAQPage`.
- **Seguridad:** headers HSTS, X-Content-Type-Options, Frame-Options, Permissions-Policy y Referrer-Policy.

## Desarrollo local

```bash
python3 -m http.server 8000
# http://localhost:8000
```

## Deploy

```bash
vercel --prod
```

## Pendientes

- [ ] Reemplazar el número de WhatsApp placeholder (`51999999999`) por el real en `index.html` (sección `#contacto`) y en el CTA.
- [ ] Conectar dominio propio si aplica (p. ej. `elhook.iaddict.pe`).

---

Hecho con 💜 — Contenido que engancha, hecho con IA.
