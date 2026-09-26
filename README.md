# Práctica de Fonética — Ejes de la Estrategia Nacional de Educación

App de práctica de pronunciación (inglés americano, IPA según Oxford Dictionary) para
concursos de fonética. Sitio estático de un solo archivo, sin dependencias externas.

## Contenido
- `index.html` — la app completa (pantalla de inicio con instrucciones + pantalla de estudio).
- `netlify.toml` — configuración de despliegue para Netlify (no requiere build).

## Cómo subirlo a GitHub

```bash
git init
git add .
git commit -m "Práctica de fonética"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/TU-REPO.git
git push -u origin main
```

## Cómo desplegarlo en Netlify

**Opción A — conectar el repositorio (recomendado):**
1. Entra a [app.netlify.com](https://app.netlify.com) → **Add new site → Import an existing project**.
2. Elige GitHub y selecciona el repositorio.
3. Build command: (déjalo vacío). Publish directory: `.`
4. Deploy site.

Cada vez que hagas `git push`, Netlify vuelve a publicar automáticamente.

**Opción B — arrastrar y soltar (más rápido, sin GitHub):**
1. Entra a [app.netlify.com/drop](https://app.netlify.com/drop).
2. Arrastra la carpeta del proyecto (o solo `index.html`) a la ventana.
3. Netlify te da la URL al instante.

## Quitar la insignia "Powered by Netlify"

Esa marca de agua la agrega Netlify automáticamente en el plan gratuito; no es parte
del código. Se puede ocultar desde **Site configuration → General → Status badges**
(o pasando a un plan con dominio propio verificado).

## Editar el contenido (palabras, oraciones, pronunciación)

Todo el contenido vive en el arreglo `DATA` dentro de `index.html` (cerca del inicio
del `<script>`). Cada palabra u oración es un par `["texto", "/pronunciación IPA/"]`.
