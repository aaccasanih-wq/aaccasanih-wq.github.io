# aaccasanih-wq.github.io

Portfolio + CV de Axel Ccasani. Sitio Jekyll deployado en GitHub Pages.

## Cómo deployear

### Opción A — Deploy en GitHub Pages (recomendado, 1 solo paso)

1. Crear en GitHub un repositorio nuevo, vacío, **exactamente con el nombre** `aaccasanih-wq.github.io` (el nombre debe coincidir para que funcione como user page).
2. Push este contenido a la rama `main` de ese repo:

```bash
cd aaccasanih-wq.github.io
git init
git add .
git commit -m "Portfolio + CV v1"
git branch -M main
git remote add origin https://github.com/aaccasanih-wq/aaccasanih-wq.github.io.git
git push -u origin main
```

3. En GitHub ir a **Settings → Pages**. Source: `Deploy from a branch`, Branch: `main`, folder: `/ (root)`. Save.
4. En 1–3 minutos el build completa. URL pública:

```
https://aaccasanih-wq.github.io
```

### Opción B — Probar localmente con Jekyll

```bash
gem install bundler jekyll
bundle init      # si no existe Gemfile aún
# agregar gem "github-pages", group: :jekyll_plugins
bundle install
bundle exec jekyll serve
# http://127.0.0.1:4000
```

## Estructura

```
aaccasanih-wq.github.io/
├── _config.yml          # configuración Jekyll
├── _layouts/
│   ├── default.html     # layout base (header + footer)
│   └── project.html     # layout de case study
├── _includes/
│   ├── header.html
│   └── footer.html
├── _data/               # (vacío, para futuro)
├── assets/
│   ├── css/style.css    # CSS del sitio (sin tema externo)
│   ├── img/             # screenshots de KAYLA y GastosBot
│   └── files/
│       ├── Axel_Ccasani_CV.pdf          # CV inglés
│       └── Axel_Ccasani_CV_espanol.pdf # CV español
├── index.md             # home
├── cv.md                # página de CV
├── kayla.md             # case study KAYLA
├── gastosbot.md         # case study GastosBot
└── uplearn.md           # case study UPLearn
```

## Páginas

| URL | Contenido |
|---|---|
| `/` | Home: hero, grid de proyectos, about |
| `/cv/` | CV completo + descarga PDF (español e inglés) |
| `/kayla/` | Case study KAYLA (salud, AI agents roadmap) |
| `/gastosbot/` | Case study GastosBot (LLM + automatización bancaria) |
| `/uplearn/` | Case study UPLearn (producto universitario, MVP) |

## Editar contenido

- Para cambiar texto de una página: edita el `.md` correspondiente (Jekyll + kramdown).
- Para cambiar estilos: edita `assets/css/style.css`.
- Para agregar una página nueva: copia `kayla.md` como template, cámbiale el frontmatter y guarda con el nombre del archivo (la URL será `/<nombre>/`).

## Stack

- **Jekyll** — soportado nativamente por GitHub Pages, sin build manual.
- **kramdown** — Markdown con sintaxis extendida (tablas, etc).
- **Sin tema externo** — todo el CSS está en `assets/css/style.css`. GitHub Pages no necesita descargar temas remotos.

## Licencia

Contenido © Axel Aaron Ccasani Huachua. Capturas de proyectos propias.