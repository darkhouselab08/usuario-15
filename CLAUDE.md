# CLAUDE.md — Memoria de trabajo del proyecto

## Proyecto
**Refugio del Cielo** — landing one-page para una cabaña-mirador off-grid en Tobía, Cundinamarca.

## Stack
Sitio estático: HTML + CSS + JS vanilla, sin build. Fuentes por Google Fonts (Fraunces + Inter).

## Convenciones
- Imágenes en `assets/img/`, estilos en `assets/css/`, scripts en `assets/js/`.
- Documentación y decisiones en `docs/`.
- Commits en formato Conventional Commits (`feat:`, `fix:`, `docs:`, `chore:`…).
- Rama principal: `main`. Trabajo por features en `feature/<descripcion>`.

## Estado actual
- Todo el CSS y JS está embebido en `index.html` (1085 líneas). Pendiente extraerlos.
- Faltan imágenes `historia1-3.jpeg` (hay fallback por `onerror`).

## Pendientes
1. Agregar imágenes de historias.
2. (Opcional) Externalizar CSS y JS.
3. Configurar deploy (GitHub Pages / Netlify).
