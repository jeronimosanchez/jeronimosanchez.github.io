# Fotos y fichas de Petal

Las fotos del catálogo de Petal, con un enlace fijo por variante (producto × color × talla), y la
descripción de cada producto.

## El enlace

    https://jeronimosanchez.github.io/petal/fotos/grande/<nombre>.webp   1.200 px, para el detalle
    https://jeronimosanchez.github.io/petal/fotos/mini/<nombre>.jpg      168 px, para la tarjeta y el Excel

`<nombre>` sale de la fila del Excel: producto, color y talla, en minúsculas, sin tildes y con
guiones. «Ramo de Peonías · Rosa · M» → `ramo-de-peonias-rosa-m`.

## Cambiar una foto

Se sube otra con el mismo nombre. El enlace no cambia y la nueva se ve en 10 minutos como mucho.
Si una variante todavía no tiene foto, el chat enseña el hueco con la flor.

## Los archivos de datos

- `fichas.json`: lo que lee el chat. La descripción de cada producto (una por producto: vale para
  todas sus tallas y colores), lo que incluye cada tipo de producto y la lista de fotos con su
  versión. La versión cambia cuando cambia la foto.
- `fotos.csv` y `fichas.csv`: lo mismo en tabla, para la pestaña «Catálogo visual» del Excel.

No se editan a mano: los genera `tools/fotos/publicar_web.py`, en el repositorio de diseño de Petal V2.

Imágenes generadas con FLUX, de Black Forest Labs.
