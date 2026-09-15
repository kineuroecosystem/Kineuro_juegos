# Kineuro_juegos

Colección de juegos de fisioterapia de Kineurog. Cada juego vive en su
propia carpeta bajo `games/` y es una app web estática (sin build), pensada
para publicarse en `kineurog.com/games/<nombre-del-juego>`.

## Juegos

- [`games/atrapa-estrellas`](games/atrapa-estrellas) — usa la cámara del
  celular/tablet como sensor de movimiento: el paciente alcanza estrellas en
  pantalla moviendo los brazos. Ver el README de esa carpeta para el detalle.

## Publicar con GitHub Pages

Este repo es público, así que GitHub Pages funciona sin plan pago:

1. En GitHub: **Settings → Pages → Build and deployment → Source**:
   elegir "Deploy from a branch".
2. **Branch**: `main`, carpeta `/(root)` → **Save**.
3. Unos minutos después queda publicado en
   `https://kineuroecosystem.github.io/kineuro_juegos/`, con "Atrapa las
   Estrellas" en `.../games/atrapa-estrellas/`.

### Para que responda en kineurog.com/games/...

Hay dos formas, según cómo esté armado el sitio principal:

- **Si kineurog.com ya usa GitHub Pages con dominio personalizado**: agregar
  un archivo `CNAME` en la raíz de este repo con `kineurog.com`, y configurar
  el registro DNS correspondiente. Esto sirve TODO el repo en la raíz del
  dominio (kineurog.com/, kineurog.com/games/atrapa-estrellas/, etc.), así
  que solo aplica si kineurog.com no tiene ya otro sitio en la raíz.
- **Si kineurog.com vive en otro hosting** (WordPress, Squarespace, Wix, un
  VPS, Cloudflare, etc.): hay que agregar ahí una regla de reverse proxy /
  rewrite que redirija las peticiones a `/games/*` hacia este sitio de
  GitHub Pages. Cómo hacerlo depende del hosting — si se cuenta con acceso a
  él, se puede armar esa regla.
