# Breathe

Página web que muestra una animación de respiración de 10 segundos antes de reabrir una red social, para cortar el uso automático de redes sociales.

## Cómo funciona

1. `docs/index.html` se publica gratis con **GitHub Pages**.
2. En **Atajos** (iPhone) creás una automatización personal por cada red social: "Instagram se abre" → **Abrir URLs** → `https://<tu-usuario>.github.io/<repo>/?return=instagram`.
3. Se abre Safari con la animación. A los 10s aparece un botón "Abrir Instagram" que te devuelve a la app vía su URL scheme (`instagram://`).

Sin Xcode, sin Mac, sin firmas que caducan, sin Apple Developer Program.

## Publicar en GitHub Pages

```bash
cd "C:\Users\Gregorio\Desktop\Claude\Breathe"
git init
git add .
git commit -m "Breathe"
git branch -M main
git remote add origin https://github.com/<tu-usuario>/<repo>.git
git push -u origin main
```

Después, en GitHub: **Settings → Pages** → Source: rama `main`, carpeta `/docs` → Save. En 1-2 minutos queda publicado en `https://<tu-usuario>.github.io/<repo>/`.

## Configurar cada red social

En Atajos → pestaña **Automatización** → **Nueva automatización personal**:

- **App** → elegí la red (ej. Instagram) → **Se abre**.
- Acción **Abrir URLs** → pegá `https://<tu-usuario>.github.io/<repo>/?return=instagram` (cambiá `instagram` por el id de cada red: `tiktok`, `twitter`, `facebook`, `snapchat`, `reddit`, `youtube`, `whatsapp`).
- Desactivá **Preguntar antes de ejecutar**.
- Repetí una automatización por app.

**Limitación de iOS** (no depende de esta implementación): Apple obliga a tocar un banner de confirmación cuando una automatización se dispara por "app se abre", así sea para abrir una URL o una app. Vas a ver la red social un instante, un banner de Atajos, lo tocás, y ahí sí aparece Breathe.

## Probar sin configurar Atajos

Abrí directamente en Safari del iPhone (o cualquier navegador):

```
https://<tu-usuario>.github.io/<repo>/?return=instagram
```

O sin parámetro, para ver la animación en modo demo (el botón final solo reinicia en vez de abrir una app):

```
https://<tu-usuario>.github.io/<repo>/
```
