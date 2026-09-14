# Directorio de Clubes PF

Buscador del directorio de los 51 clubes de Planet Fitness México que opera Fitness Para Todos:
contacto del club, equipo, IDs de Zenoti y Planet Fitness, ubicación, administración de la plaza,
mantenimiento y horario.

Es una sola página estática (`index.html`) con los datos incluidos. No usa servidor, base de
datos ni dependencias; solo carga tipografías de Google Fonts.

Responsable: Jesús Garduño Montiel, Infraestructura y Servicios TI.

---

## Antes de publicar

**GitHub Pages publica en internet abierto.** Cualquiera con la liga ve la página, aunque el
repositorio sea privado. `index.html` lleva teléfonos celulares de gerentes, subgerentes y
técnicos, y contactos de administradores de plaza.

- Publícalo dentro de la organización de FPT en GitHub, no en una cuenta personal.
- La página trae `<meta name="robots" content="noindex,nofollow">`, que le pide a los
  buscadores no listarla. Es una petición, no un control de acceso.
- Quitar el archivo después no lo borra del historial del repositorio.
- Con cuenta gratuita, Pages exige repositorio **público**, y entonces el archivo también
  queda a la vista en el repo. Con Pro, Team o Enterprise el repo puede ser privado.

## Publicar

### Opción A: con git (el repositorio ya trae su primer commit)

1. En GitHub crea un repositorio **vacío**, sin README, sin `.gitignore` y sin licencia.
   Por ejemplo `directorio-clubes`.
2. Dentro de esta carpeta:

   ```bash
   git remote add origin https://github.com/<organizacion>/directorio-clubes.git
   git push -u origin main
   ```

3. Sigue con **Activar Pages**, abajo.

### Opción B: desde el navegador, sin git

1. En GitHub crea el repositorio, por ejemplo `directorio-clubes`.
2. **Add file → Upload files** y arrastra estos tres archivos:
   `index.html`, `README.md` y `.nojekyll`.
   No subas la carpeta `.git`. Si tu explorador oculta `.nojekyll`, la página funciona igual
   sin él.
3. **Commit changes**.

### Activar Pages

1. **Settings → Pages**.
2. En *Source*: **Deploy from a branch**, rama `main`, carpeta `/ (root)`, **Save**.
3. En uno o dos minutos la página queda en
   `https://<organizacion>.github.io/directorio-clubes/`.
   La liga aparece en esa misma pantalla.

## Actualizar

El directorio sale del Excel *Directorio de clubs.xlsx*. Cuando cambia, se regenera
`index.html` y se sube de nuevo (con `git commit` + `git push`, o con
**Add file → Upload files** en el navegador). La liga no cambia.

## Contenido

| Archivo | Para qué |
|---|---|
| `index.html` | La página completa con los datos. Es lo único indispensable. |
| `.nojekyll` | Le dice a GitHub Pages que sirva el archivo tal cual, sin procesarlo con Jekyll. |
| `.gitattributes` | Fija saltos de línea LF para que el repo no cambie entre Windows y Mac. |
| `README.md` | Este documento. |
