# Carles Soler — Landing personal

Sitio estático de una sola página. Sin build, sin dependencias locales.

- `index.html` — toda la landing.
- Tailwind se carga vía CDN.
- Inter + JetBrains Mono vía Google Fonts.

## Despliegue en GitHub Pages

1. **Crea el repositorio** en GitHub. Recomendado: nombre `carles-soler.github.io` (sustituyendo `carles-soler` por tu usuario real). Así la web vivirá en `https://<tu-usuario>.github.io/`.

   > Si prefieres otro nombre (ej. `portfolio`), la URL será `https://<tu-usuario>.github.io/portfolio/`.

2. **Sube los archivos** desde esta carpeta (`C:\Users\34663\Desktop\landing-page`):

   ```powershell
   cd "C:\Users\34663\Desktop\landing-page"
   git init
   git add .
   git commit -m "Initial commit: landing page"
   git branch -M main
   git remote add origin https://github.com/<tu-usuario>/<tu-repo>.git
   git push -u origin main
   ```

3. **Activa Pages**: en GitHub → `Settings` → `Pages` → *Source*: `Deploy from a branch` → Branch: `main` / carpeta `/ (root)` → `Save`.

4. **Espera 1-2 minutos** y abre la URL que te indique GitHub Pages.

## Personalizaciones rápidas

- **Email / teléfono / LinkedIn**: edita la sección `#contacto` y el hero.
- **Métricas del hero**: bloque `<dl>` con `grid grid-cols-2 ... sm:grid-cols-4`.
- **Color de acento**: variable `accent.500` (`#7c8cff`) dentro del bloque `tailwind.config`.
- **Fuente**: cambia `Inter` por `Roboto` en el `<link>` de Google Fonts y en `fontFamily.sans`.

## Notas

- El CDN de Tailwind no es lo más rápido posible, pero para una landing personal estática es perfecto (cero build, cero CI).
- Si más adelante quieres optimizar: migrar a Tailwind CLI o a un build con Vite y servir el CSS compilado.
