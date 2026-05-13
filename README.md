# Copy Estratega — Propuestas (deploy a GitHub Pages)

Carpeta lista para subir a un repo y servirse vía GitHub Pages.

## Estructura

```
gh-pages-deploy/
├── .nojekyll           ← evita que GitHub procese con Jekyll
├── index.html          ← landing con cards a las 2 propuestas
├── README.md           ← este archivo
├── viron/
│   ├── index.html      ← Viron Sales Deck
│   ├── deck-stage.js
│   ├── colors_and_type.css
│   ├── logo-circle.png
│   └── daniel-photo.png
└── bildenlex/
    ├── index.html      ← Bildenlex Sales Deck
    ├── deck-stage.js
    ├── colors_and_type.css
    ├── logo-circle.png
    ├── daniel-photo.png
    └── bildenlex-logo.png
```

## Deploy en GitHub Pages — 60 segundos

1. Ir a [github.com/new](https://github.com/new) → crear un repo, p.ej. `propuestas` (público o privado, ambos funcionan con Pages en plan gratuito).
2. En la página del repo recién creado, clic en **"uploading an existing file"** (link gris bajo el `quick setup` box).
3. **Arrastrar todo el contenido de esta carpeta `gh-pages-deploy/`** (los archivos sueltos, no la carpeta envolvente) a la zona de upload.
4. Commit directo a `main` con el mensaje que quieras.
5. Ir a **Settings → Pages**.
6. En **"Build and deployment"** → **Source**: `Deploy from a branch`.
7. **Branch**: `main` · **Folder**: `/ (root)` · clic en **Save**.
8. Esperar ~30 segundos. El banner de arriba mostrará la URL pública:
   - `https://<tu-usuario>.github.io/propuestas/`
   - Landing con las 2 cards.
   - `/viron/` para el deck de Viron.
   - `/bildenlex/` para el deck de Bildenlex.

## URLs resultantes

Suponiendo `<usuario>` = tu usuario de GitHub y `<repo>` = el nombre del repo:

- `https://<usuario>.github.io/<repo>/` — landing
- `https://<usuario>.github.io/<repo>/viron/` — Viron Sales Deck
- `https://<usuario>.github.io/<repo>/bildenlex/` — Bildenlex Sales Deck

## Notas

- Los decks están escalados a 1920×1080 vía `deck-stage.js`; en cualquier viewport se ajustan con letterboxing.
- Navegación: flechas ←/→ del teclado, tap en los bordes (móvil), o el indicador de slide en la esquina.
- Cero dependencias de backend — todo es estático. Funciona offline si lo descargan.
