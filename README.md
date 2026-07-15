# Refugio del Cielo

Landing one-page para **Refugio del Cielo**, una cabaña-mirador off-grid en Tobía, Cundinamarca. Internet Starlink garantizado, energía solar y vista de 180° al valle. Enfocada a nómadas digitales y parejas.

## Stack

Sitio estático: HTML + CSS + JavaScript vanilla. Sin dependencias de build. Fuentes vía Google Fonts (Fraunces + Inter).

## Estructura

```
refugio-del-cielo/
├── index.html          # Landing (por ahora CSS y JS embebidos)
├── assets/
│   ├── img/            # Imágenes del sitio (deck, vista, panorama, historia1-3…)
│   ├── css/            # Estilos externos (al extraer el <style> de index.html)
│   ├── js/             # Scripts externos (al extraer el <script>)
│   └── fonts/          # Fuentes locales (opcional)
├── docs/               # Brief de diseño, notas, decisiones
├── .github/            # Workflows / plantillas (CI, deploy a Pages)
├── .gitignore
└── README.md
```

## Desarrollo local

No requiere build. Basta abrir `index.html` en el navegador, o servir la carpeta:

```bash
python3 -m http.server 8000
# luego abre http://localhost:8000
```

## Pendientes

- Agregar imágenes faltantes: `historia1.jpeg`, `historia2.jpeg`, `historia3.jpeg` en `assets/img/`.
- (Opcional) Extraer el `<style>` a `assets/css/styles.css` y el `<script>` a `assets/js/main.js`.
- Configurar deploy (GitHub Pages / Netlify).
