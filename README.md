# CAJ — Visualizaciones

Sitio Hugo con dos visualizaciones interactivas sobre los Centros de Acceso a
Justicia (CAJ) de Argentina:

- **`static/viz/cajs_mapa_apertura.html`** — mapa (Leaflet) de la apertura de cada
  CAJ por año y ubicación, con línea de tiempo.
- **`static/viz/subtema_mapa.html`** — treemap (Plotly) de las consultas por tema y
  subtema (nomenclatura histórica continua), con filtros.

La página de inicio (`layouts/index.html` + `content/_index.md`) las incrusta con
`iframe`.

## Uso

```bash
hugo server        # previsualizar en http://localhost:1313
hugo               # generar el sitio en ./public
```

Antes de publicar, ajustá `baseURL` en `hugo.toml` a la URL real del sitio.

Las visualizaciones cargan librerías (Plotly, Leaflet) y teselas de mapa desde
CDNs, por lo que requieren conexión a internet al visualizarse.
