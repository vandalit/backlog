# backlog

SPA de **roadmap tipo Gantt**: vista horizontal de proyectos en el tiempo, con
barras interactivas que despliegan cards de detalle y un sistema de etiquetas
**PKM** para conectar proyectos por categorías y verticales.

## Estado actual: stub

Mock visual autocontenido, sin dependencias. Dark mode por defecto y barras en
paleta cítrica saturada.

- **`index.html`** — raíz, redirige al stub.
- **`stub/index.html`** — el mock del Gantt (HTML/CSS/JS en un solo archivo).

Los datos viven en el array `PROJECTS` dentro de `stub/index.html`. La
cronología es ficticia (Ene–Dic) y se ajustará a fechas reales más adelante.

### Cómo verlo

Abre `index.html` en el navegador, o sirve la carpeta:

```bash
python3 -m http.server 8000
# → http://localhost:8000
```

### Qué incluye el stub

- 6 proyectos mock dispuestos en escalera, con solapamientos y un máximo de 3
  proyectos en paralelo por tramo.
- Barras clickeables que abren un panel de detalle (avance, responsable,
  presupuesto, descripción, tags).
- Barra de filtros PKM: verticales (◆) y categorías (#). Al activar una
  etiqueta se resaltan los proyectos conectados.

## Siguiente fase (planeado)

SPA con **frontend y backend separados**:

- `frontend/` — la SPA (framework a definir), consumiendo la API.
- `backend/` — API que sirve proyectos, tramos y etiquetas.

El stub está hecho data-driven a propósito para que migrar a datos reales del
backend sea directo.
