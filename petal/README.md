# Fotos y fichas de Petal

Las fotos del catálogo de Petal, con un enlace fijo por variante (producto × color × talla).

## El enlace

    https://jeronimosanchez.github.io/petal/fotos/grande/<nombre>.webp   1.200 px, para el detalle
    https://jeronimosanchez.github.io/petal/fotos/mini/<nombre>.jpg      168 px, para la tarjeta y el Excel

`<nombre>` sale de la fila del Excel: producto, color y talla, en minúsculas, sin tildes y con
guiones. «Ramo de Peonías · Rosa · M» → `ramo-de-peonias-rosa-m`.

## Cambiar una foto

Se sube otra con el mismo nombre. El enlace no cambia y la nueva se ve en 10 minutos como mucho.
Si una variante todavía no tiene foto, el chat enseña el hueco con la flor.

## fichas.json

La descripción de cada producto (una por producto: vale para todas sus tallas y colores), lo que
incluye cada tipo de producto y la lista de fotos publicadas con su versión. La versión cambia
cuando cambia la foto; así el chat y el Excel saben que tienen que volver a cargarla.

No se edita a mano: lo genera `tools/fotos/publicar_web.py`, en el repositorio de diseño de Petal V2.

Imágenes generadas con FLUX, de Black Forest Labs.
