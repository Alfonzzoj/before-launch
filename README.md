# Before Launch 🚀 / Antes del Lanzamiento 🚀

**Pre-launch verification rules for any website.**
**Reglas de verificación previas al lanzamiento de cualquier sitio web.**

> 📖 This document is bilingual: **[English](#-english)** · **[Español](#-español)**

---

## 🇬🇧 English

### Purpose

A checklist of rules you **must** verify before taking a site to production. Every rule is a gate: if it fails, do not launch.

### 1. Functionality / Funcionalidad

- [ ] All links work (no `404`, no `#` placeholders)
- [ ] All forms submit correctly, validate input and show success/error feedback
- [ ] Emails triggered by forms are received (check spam)
- [ ] Search, filters, pagination and cart/checkout flows work end-to-end
- [ ] 404, 500 and maintenance pages exist and are styled
- [ ] Old URLs have `301` redirects to their new locations
- [ ] Third-party embeds (maps, video, widgets) load correctly

### 2. SEO

- [ ] `<title>` and `<meta name="description">` unique per page
- [ ] One single `h1` per page, heading hierarchy is logical
- [ ] `sitemap.xml` generated and submitted
- [ ] `robots.txt` allows crawling of public pages and blocks staging
- [ ] Canonical URLs set (no duplicate content)
- [ ] Open Graph + Twitter Card images render correctly
- [ ] Structured data (Schema.org) validates without errors
- [ ] No `noindex` tags left from staging
- [ ] Images have descriptive `alt` attributes

### 3. Performance ⚡

- [ ] Core Web Vitals in green: **LCP < 2.5s**, **INP < 200ms**, **CLS < 0.1**
- [ ] Images optimized (WebP/AVIF, resized, lazy-loaded)
- [ ] CSS/JS minified, code-split and tree-shaken
- [ ] Fonts preloaded, `font-display: swap`, subset if possible
- [ ] Static assets cached with long `Cache-Control` + hashed filenames
- [ ] HTML responses compressed (Brotli/Gzip)
- [ ] Tested on slow 4G and a mid-range phone

### 4. Security 🔒

- [ ] HTTPS everywhere, valid certificate, no mixed content
- [ ] HSTS header enabled
- [ ] Security headers set: `Content-Security-Policy`, `X-Frame-Options`, `X-Content-Type-Options`, `Referrer-Policy`
- [ ] No secrets, API keys or tokens in the repo or client bundle
- [ ] All dependencies audited (`npm audit`, `pip-audit`, etc.) — no critical CVEs
- [ ] Forms protected against spam (honeypot/rate limiting) and injection (XSS, SQLi)
- [ ] File uploads restricted by type and size
- [ ] Admin panels behind strong auth + 2FA, default credentials changed

### 5. Legal & Compliance ⚖️

- [ ] Privacy policy published and linked
- [ ] Cookie banner + consent (GDPR/ePrivacy), before any tracking script loads
- [ ] Cookie policy and terms of service available
- [ ] Cookie/analytics consent remembered and revocable
- [ ] Copyright, licenses and attributions for assets/fonts/plugins
- [ ] Data deletion/export requests have a defined process

### 6. Accessibility (WCAG 2.1 AA) ♿

- [ ] Full keyboard navigation, visible focus states
- [ ] Color contrast ratio ≥ **4.5:1** (text) / **3:1** (large text)
- [ ] Meaningful `alt` text, labels tied to inputs, `aria-*` where needed
- [ ] Tested with a screen reader (VoiceOver / NVDA)
- [ ] Motion can be paused (respects `prefers-reduced-motion`)
- [ ] Errors announced, not only shown by color

### 7. Responsive & Browsers 📱

- [ ] Layout verified at 320 / 375 / 768 / 1024 / 1440 / 1920 px
- [ ] Tested on iOS Safari + Chrome and Android Chrome
- [ ] Cross-browser: latest Chrome, Firefox, Safari, Edge
- [ ] Touch targets ≥ 44×44 px, no horizontal scroll
- [ ] `100vh`/`dvh` mobile viewport issues handled

### 8. Content & Copy ✍️

- [ ] Zero typos, correct language/country variant (es-ES vs es-MX, en-US vs en-GB)
- [ ] Placeholder/lorem text removed
- [ ] Images not stretched, correct attribution
- [ ] Favicon, app icons, `apple-touch-icon`, `og:image` present
- [ ] Contact info, address, phone and social links are real and current

### 9. Analytics, Monitoring & Ops 📊

- [ ] Analytics (GA4/Plausible/Matomo) firing, with consent mode
- [ ] Conversion events and goals verified
- [ ] Error tracking active (Sentry, LogRocket…)
- [ ] Uptime monitoring + alerts configured
- [ ] Server logs and 404 reports are being collected
- [ ] Automated backups configured and **restore tested**
- [ ] Staging/dev environment blocked from indexing and from public access

### 10. Deployment & Domain 🌐

- [ ] DNS records correct (A/AAAA/CNAME), TTL propagated
- [ ] Domain not expiring soon; auto-renew on
- [ ] CDN configured, cache purge done
- [ ] `.env`/config values verified for production (correct DB, no test keys)
- [ ] Rollback plan documented; deployment reproducible
- [ ] Load/stress test passed for expected traffic

---

## 🇪🇸 Español

### Propósito

Lista de verificación de reglas que **debes** cumplir antes de llevar un sitio a producción. Cada regla es una compuerta: si falla, no se lanza.

### 1. Funcionalidad

- [ ] Todos los enlaces funcionan (sin `404`, sin `#` de relleno)
- [ ] Todos los formularios envían, validan y muestran éxito/error
- [ ] Los correos disparados por formularios llegan (revisar spam)
- [ ] Búsqueda, filtros, paginación y carrito/checkout funcionan de punta a punta
- [ ] Existen las páginas 404, 500 y de mantenimiento, y están estilizadas
- [ ] Las URLs antiguas tienen redirecciones `301` a su nueva ubicación
- [ ] Los embeds externos (mapas, video, widgets) cargan correctamente

### 2. SEO

- [ ] `<title>` y `<meta name="description">` únicos por página
- [ ] Un solo `h1` por página y jerarquía de encabezados lógica
- [ ] `sitemap.xml` generado y enviado
- [ ] `robots.txt` permite rastrear páginas públicas y bloquea staging
- [ ] URLs canónicas configuradas (sin contenido duplicado)
- [ ] Open Graph + Twitter Card se renderizan bien
- [ ] Datos estructurados (Schema.org) validan sin errores
- [ ] Sin etiquetas `noindex` residuales del staging
- [ ] Imágenes con atributos `alt` descriptivos

### 3. Rendimiento ⚡

- [ ] Core Web Vitals en verde: **LCP < 2.5s**, **INP < 200ms**, **CLS < 0.1**
- [ ] Imágenes optimizadas (WebP/AVIF, redimensionadas, lazy-load)
- [ ] CSS/JS minificados, code-split y tree-shaking
- [ ] Fuentes con preload, `font-display: swap`, subconjuntadas si es posible
- [ ] Assets estáticos con caché largo (`Cache-Control`) y nombres con hash
- [ ] Respuestas HTML comprimidas (Brotli/Gzip)
- [ ] Probado en 4G lento y en un teléfono gama media

### 4. Seguridad 🔒

- [ ] HTTPS en todo el sitio, certificado válido, sin contenido mixto
- [ ] HSTS habilitado
- [ ] Cabeceras: `Content-Security-Policy`, `X-Frame-Options`, `X-Content-Type-Options`, `Referrer-Policy`
- [ ] Sin secretos, API keys ni tokens en el repo ni en el bundle del cliente
- [ ] Dependencias auditadas (`npm audit`, `pip-audit`, …) — sin CVEs críticas
- [ ] Formularios protegidos contra spam (honeypot/limitación) e inyección (XSS, SQLi)
- [ ] Subidas de archivo restringidas por tipo y tamaño
- [ ] Paneles de administración con autenticación fuerte + 2FA, credenciales por defecto cambiadas

### 5. Legal y Cumplimiento ⚖️

- [ ] Política de privacidad publicada y enlazada
- [ ] Banner de cookies + consentimiento (GDPR/ePrivacy) **antes** de cargar cualquier script de tracking
- [ ] Política de cookies y términos y condiciones disponibles
- [ ] El consentimiento se recuerda y se puede revocar
- [ ] Licencias y atribuciones de assets/fuentes/plugins
- [ ] Proceso definido para solicitudes de borrado/exportación de datos

### 6. Accesibilidad (WCAG 2.1 AA) ♿

- [ ] Navegación completa por teclado, foco visible
- [ ] Contraste de color ≥ **4.5:1** (texto) / **3:1** (texto grande)
- [ ] Textos `alt` con sentido, etiquetas ligadas a inputs, `aria-*` cuando toca
- [ ] Probado con lector de pantalla (VoiceOver / NVDA)
- [ ] Se puede pausar el movimiento (`prefers-reduced-motion`)
- [ ] Los errores se anuncian, no solo se muestran por color

### 7. Responsive y Navegadores 📱

- [ ] Layout verificado a 320 / 375 / 768 / 1024 / 1440 / 1920 px
- [ ] Probado en iOS Safari + Chrome y Android Chrome
- [ ] Multi-navegador: Chrome, Firefox, Safari, Edge (últimas versiones)
- [ ] Objetos táctiles ≥ 44×44 px, sin scroll horizontal
- [ ] Resueltos los problemas de `100vh`/`dvh` en móvil

### 8. Contenido y Copy ✍️

- [ ] Cero erratas, variante lingüística/país correcta (es-ES vs es-MX, en-US vs en-GB)
- [ ] Sin texto de relleno ni lorem ipsum
- [ ] Imágenes sin deformar, con atribución correcta
- [ ] Favicon, iconos de app, `apple-touch-icon`, `og:image` presentes
- [ ] Datos de contacto, dirección, teléfono y redes sociales reales y actualizados

### 9. Analítica, Monitoreo y Ops 📊

- [ ] Analítica (GA4/Plausible/Matomo) disparando, con modo de consentimiento
- [ ] Eventos y objetivos de conversión verificados
- [ ] Error tracking activo (Sentry, LogRocket…)
- [ ] Monitoreo de uptime + alertas configuradas
- [ ] Logs del servidor y reportes de 404 en recolección
- [ ] Backups automáticos configurados y **restauración probada**
- [ ] Entorno staging/dev bloqueado para indexación y de acceso público

### 10. Despliegue y Dominio 🌐

- [ ] Registros DNS correctos (A/AAAA/CNAME), TTL propagado
- [ ] Dominio sin vencer pronto; renovación automática activada
- [ ] CDN configurado y caché purgada
- [ ] Valores `.env`/config verificados para producción (BD correcta, sin claves de prueba)
- [ ] Plan de rollback documentado; despliegue reproducible
- [ ] Prueba de carga/estrés superada para el tráfico esperado

---

## 🚦 Launch Gate / Compuerta de Lanzamiento

Launch **only** when every box is checked:

```text
BLOCKER  → any failing rule in: Funcionalidad · Seguridad · Legal · Despliegue
MAJOR    → any failing rule in: SEO · Rendimiento · Accesibilidad · Analítica
MINOR    → Content, browser quirks, cosmetics (fix within 48h of launch)
```

```text
Lanza SOLO cuando todas las casillas estén marcadas:

BLOCKER  → cualquier regla fallida en: Funcionalidad · Seguridad · Legal · Despliegue
MAJOR    → cualquier regla fallida en: SEO · Rendimiento · Accesibilidad · Analítica
MINOR    → contenido, particularidades de navegador, estética (arreglar en 48h)
```

### Final sign-off / Aprobación final

| Role / Rol | Name / Nombre | Date / Fecha |
|---|---|---|
| Developer / Desarrollador |  |  |
| Designer / Diseñador |  |  |
| QA |  |  |
| Owner / Cliente |  |  |

---

### Changelog

| Date | Change |
|---|---|
| 2026-10-19 | Initial bilingual checklist |
