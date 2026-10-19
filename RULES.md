# Launch Rules ✅

Pre-launch verification rules. One list, one purpose: **if a rule fails, do not launch.**
Reglas de verificación previas al lanzamiento. Una sola lista, un solo propósito: **si una regla falla, no se lanza.**

Severity / Severidad: `BLOCKER` (must pass) · `MAJOR` (must pass) · `MINOR` (fix within 48h / arreglar en 48h)

---

## 1. Functionality / Funcionalidad — `BLOCKER`

- [ ] All links work, no `404`, no `#` placeholders / Todos los enlaces funcionan, sin `404` ni `#` de relleno
- [ ] All forms submit, validate and show success/error feedback / Todos los formularios envían, validan y muestran éxito/error
- [ ] Triggered emails arrive (check spam) / Los correos disparados llegan (revisar spam)
- [ ] Search, filters, pagination and checkout work end-to-end / Búsqueda, filtros, paginación y checkout funcionan de punta a punta
- [ ] 404, 500 and maintenance pages exist and are styled / Existen 404, 500 y mantenimiento, y están estilizadas
- [ ] Old URLs have `301` redirects to their new location / URLs antiguas con redirección `301` a su nueva ubicación
- [ ] Third-party embeds (maps, video, widgets) load correctly / Embeds externos cargan correctamente

## 2. SEO — `MAJOR`

- [ ] Unique `<title>` and `<meta name="description">` per page / `<title>` y `<meta description>` únicos por página
- [ ] One `h1` per page, logical heading hierarchy / Un solo `h1` por página y jerarquía de encabezados lógica
- [ ] `sitemap.xml` generated and submitted / `sitemap.xml` generado y enviado
- [ ] `robots.txt` allows public crawling and blocks staging / `robots.txt` permite páginas públicas y bloquea staging
- [ ] Canonical URLs set, no duplicate content / URLs canónicas sin contenido duplicado
- [ ] Open Graph + Twitter Card render correctly / Open Graph + Twitter Card se renderizan bien
- [ ] Structured data (Schema.org) validates without errors / Datos estructurados validan sin errores
- [ ] No leftover `noindex` tags from staging / Sin `noindex` residuales del staging
- [ ] Images have descriptive `alt` attributes / Imágenes con `alt` descriptivos

## 3. Performance ⚡ — `MAJOR`

- [ ] Core Web Vitals green: LCP < 2.5s, INP < 200ms, CLS < 0.1 / Core Web Vitals en verde
- [ ] Images optimized (WebP/AVIF, resized, lazy-loaded) / Imágenes optimizadas (WebP/AVIF, redimensionadas, lazy-load)
- [ ] CSS/JS minified, code-split, tree-shaken / CSS/JS minificados, code-split, tree-shaking
- [ ] Fonts preloaded, `font-display: swap`, subsetted / Fuentes con preload, `font-display: swap`, subconjuntadas
- [ ] Long `Cache-Control` on hashed static assets / Caché largo en assets con hash
- [ ] HTML compressed (Brotli/Gzip) / HTML comprimido (Brotli/Gzip)
- [ ] Tested on slow 4G and a mid-range phone / Probado en 4G lento y teléfono gama media

## 4. Security 🔒 — `BLOCKER`

- [ ] HTTPS everywhere, valid certificate, no mixed content / HTTPS en todo, certificado válido, sin contenido mixto
- [ ] HSTS header enabled / HSTS habilitado
- [ ] Headers set: `Content-Security-Policy`, `X-Frame-Options`, `X-Content-Type-Options`, `Referrer-Policy` / Cabeceras de seguridad configuradas
- [ ] No secrets, API keys or tokens in repo or client bundle / Sin secretos ni tokens en el repo ni en el bundle
- [ ] Dependencies audited, no critical CVEs / Dependencias auditadas sin CVEs críticas
- [ ] Forms protected against spam and injection (XSS, SQLi) / Formularios protegidos contra spam e inyección
- [ ] File uploads restricted by type and size / Subidas restringidas por tipo y tamaño
- [ ] Admin panels behind strong auth + 2FA, default credentials changed / Admin con 2FA y credenciales por defecto cambiadas

## 5. Legal & Compliance ⚖️ — `BLOCKER`

- [ ] Privacy policy published and linked / Política de privacidad publicada y enlazada
- [ ] Cookie banner + consent (GDPR/ePrivacy) loads before any tracking script / Banner de cookies antes de cualquier script de tracking
- [ ] Cookie policy and terms of service available / Política de cookies y términos disponibles
- [ ] Consent is remembered and revocable / El consentimiento se recuerda y se puede revocar
- [ ] Licenses/attribution for assets, fonts and plugins / Licencias y atribuciones de assets, fuentes y plugins
- [ ] Process defined for data deletion/export requests / Proceso para borrado/exportación de datos

## 6. Accessibility WCAG 2.1 AA ♿ — `MAJOR`

- [ ] Full keyboard navigation with visible focus states / Navegación por teclado con foco visible
- [ ] Contrast ≥ 4.5:1 (text) / ≥ 3:1 (large text) / Contraste ≥ 4.5:1 texto, ≥ 3:1 texto grande
- [ ] Meaningful `alt`, labels tied to inputs, `aria-*` where needed / `alt`, etiquetas y `aria-*` correctos
- [ ] Tested with a screen reader (VoiceOver / NVDA) / Probado con lector de pantalla
- [ ] Motion pausable, respects `prefers-reduced-motion` / Movimiento pausable según `prefers-reduced-motion`
- [ ] Errors announced, not conveyed by color alone / Errores anunciados, no solo por color

## 7. Responsive & Browsers 📱 — `MAJOR`

- [ ] Layout verified at 320 / 375 / 768 / 1024 / 1440 / 1920 px / Layout verificado a 320/375/768/1024/1440/1920 px
- [ ] Tested on iOS Safari + Chrome and Android Chrome / Probado en iOS Safari + Chrome y Android Chrome
- [ ] Latest Chrome, Firefox, Safari and Edge / Últimos Chrome, Firefox, Safari y Edge
- [ ] Touch targets ≥ 44×44 px, no horizontal scroll / Objetos táctiles ≥ 44×44 px, sin scroll horizontal
- [ ] Mobile viewport issues (`100vh`/`dvh`) handled / Problemas de viewport móvil resueltos

## 8. Content & Copy ✍️ — `MINOR`

- [ ] Zero typos, correct language variant (es-ES/es-MX, en-US/en-GB) / Cero erratas, variante de idioma correcta
- [ ] No placeholder or lorem ipsum text / Sin textos de relleno
- [ ] Images not distorted, correct attribution / Imágenes sin deformar y con atribución
- [ ] Favicon, app icons, `apple-touch-icon`, `og:image` present / Favicon, iconos, `apple-touch-icon`, `og:image` presentes
- [ ] Contact info, address, phone and social links are real and current / Contacto y redes reales y actualizados

## 9. Analytics, Monitoring & Ops 📊 — `MAJOR`

- [ ] Analytics firing with consent mode / Analítica disparando con modo de consentimiento
- [ ] Conversion events and goals verified / Eventos de conversión verificados
- [ ] Error tracking active (Sentry, LogRocket…) / Error tracking activo
- [ ] Uptime monitoring + alerts configured / Monitoreo de uptime + alertas
- [ ] Server logs and 404 reports collected / Logs y reportes de 404 recolectados
- [ ] Automated backups configured and restore tested / Backups automáticos y restauración probada
- [ ] Staging/dev blocked from indexing and public access / Staging bloqueado de indexación y acceso público

## 10. Deployment & Domain 🌐 — `BLOCKER`

- [ ] DNS records correct (A/AAAA/CNAME), TTL propagated / Registros DNS correctos y TTL propagado
- [ ] Domain not expiring soon, auto-renew on / Dominio sin vencer pronto, renovación automática activa
- [ ] CDN configured, cache purged / CDN configurado y caché purgada
- [ ] Production config verified (correct DB, no test keys) / Configuración de producción verificada
- [ ] Rollback plan documented, deployment reproducible / Plan de rollback documentado
- [ ] Load/stress test passed for expected traffic / Prueba de carga superada

---

## Launch Gate / Compuerta de Lanzamiento

```text
BLOCKER → any failing rule in 1, 4, 5, 10  → NO LAUNCH / NO LANZAR
MAJOR   → any failing rule in 2, 3, 6, 7, 9 → FIX BEFORE LAUNCH / ARREGLAR ANTES DE LANZAR
MINOR   → failing rules in 8                → FIX WITHIN 48H / ARREGLAR EN 48H
```

**All boxes checked = launch approved.**
**Todas las casillas marcadas = lanzamiento aprobado.**
