# José L. Mendoza Valdés — página docente

Sitio estático publicado con GitHub Pages en **https://joselmendozav.github.io/**.

| Archivo | Contenido |
|---|---|
| `index.html` | Versión en español (CSS incluido en el `<style>`) |
| `index-en.html` | Versión en inglés (mismo contenido traducido) |
| `foto.jpg` | Foto de perfil (también se usa como imagen Open Graph) |

No hay build ni dependencias: se editan los HTML, se hace commit y push a `main`, y GitHub Pages publica los cambios en uno o dos minutos.

> Cada cambio de contenido debe hacerse **en los dos archivos** (`index.html` e `index-en.html`).

## Agregar una publicación

En la sección `<!-- PUBLICACIONES -->` (o `PUBLICATIONS` en inglés), copia un bloque `<li class="pub">` y pégalo en su posición (de la más reciente a la más antigua). La numeración es automática.

Solo se muestran las **5 más recientes**: las demás siguen en el HTML pero ocultas por la regla `.pubs .pub:nth-child(n+6) { display: none; }` del `<style>`. Al agregar una nueva arriba, la más antigua visible se oculta sola. Para mostrar más, cambia el `6` por otro número (o borra la regla para mostrarlas todas).

```html
<li class="pub">
  <h3>Título del artículo</h3>
  <p class="authors">Apellido A, <span class="me">Mendoza-Valdés JL</span>, Apellido B.</p>
  <p class="venue"><em>Nombre de la revista o congreso</em>, vol(n), páginas, 2027.</p>
  <div class="tags">
    <span class="badge">Q1</span> <!-- opcional -->
    <a class="doi" href="https://doi.org/10.xxxx/xxxxx" target="_blank" rel="noopener noreferrer">DOI: 10.xxxx/xxxxx <svg class="icon" aria-hidden="true"><use href="#i-ext"/></svg><span class="sr-only"> (abre en pestaña nueva)</span></a>
  </div>
</li>
```

En `index-en.html` cambia el texto oculto por `(opens in a new tab)`.

## Agregar un curso

En la sección `<!-- DOCENCIA -->` (`TEACHING`), agrega una línea a la lista:

```html
<li>Nombre de la asignatura</li>
```

La lista se reparte sola en dos columnas. En el HTML hay un comentario que explica cómo convertirla en una tabla por semestre.

## Actualizar la fecha

Cambia la línea del pie de página (`<footer>`) en ambos archivos.

## Vista previa local

Abre `index.html` en el navegador, o ejecuta `python3 -m http.server` y visita http://localhost:8000.
