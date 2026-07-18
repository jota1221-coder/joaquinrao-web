# Deploy — Landing de Joaquín

La página es un solo `index.html` estático. No hay build ni dependencias, así que se sube a cualquier hosting estático. Tres caminos, de más recomendado a más rápido.

## Opción A — GitHub + Vercel (recomendada)

Versionado + redeploy automático en cada cambio.

1. Tené el repo en GitHub (si querés, lo dejo pusheado yo con `gh`).
2. Entrá a [vercel.com](https://vercel.com) → **Add New → Project** → importá el repo.
3. Framework Preset: **Other** (es estático). Dejá el root como está. **Deploy**.
4. Listo: te da una URL `*.vercel.app`. Cada `git push` a `main` redeploya solo.

## Opción B — Vercel por consola (rápida, sin importar repo)

Desde esta carpeta:

```
npx vercel          # primera vez pide login (abre el navegador); aceptá los defaults
npx vercel --prod   # publica la versión final
```

## Opción C — Netlify Drop (sin consola)

Entrá a [app.netlify.com/drop](https://app.netlify.com/drop) y arrastrá esta carpeta. Queda online al instante.

---

## Dominio propio (ej: joaquinrao.com.ar)

1. Comprá el dominio en tu registrador (NIC Argentina para `.com.ar`).
2. En Vercel → tu proyecto → **Settings → Domains** → agregá `joaquinrao.com.ar`.
3. Vercel te muestra qué registro apuntar (A o CNAME). Cargalo en el DNS del registrador.
4. En 10–60 min propaga y queda con HTTPS automático.

## Pendiente al tener el dominio

En `index.html`, completar las meta tags de previsualización del link:
- `og:url` con la URL final.
- `og:image` con una imagen de preview (te la puedo generar cuando llegue el momento).
