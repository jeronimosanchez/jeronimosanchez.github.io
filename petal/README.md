# Fotos y fichas de Petal

Las fotos del catálogo de Petal, con un enlace fijo para cada una de las variantes del Inventario
(producto × color × talla), y la descripción de cada producto.

## El enlace

    https://jeronimosanchez.github.io/petal/fotos/grande/<nombre>.webp   1.200 px, para el detalle
    https://jeronimosanchez.github.io/petal/fotos/mini/<nombre>.jpg      168 px, para la tarjeta y el Excel

`<nombre>` sale de la fila del Excel: producto, color y talla, en minúsculas, sin tildes y con
guiones. «Ramo de Peonías · Rosa · M» → `ramo-de-peonias-rosa-m`.

Todas las variantes tienen su enlace. Las que aún no tienen foto enseñan el hueco del sistema de
diseño: una flor con el tono de su color.

## Cambiar una foto

Se sube otra con el mismo nombre. El enlace no cambia y la nueva se ve en 10 minutos como mucho.

## Los archivos de datos

- `fichas.json`: lo que lee el chat. La descripción de cada producto y talla
  (`productos["<Producto>"].tallas["<Talla>"]`; vale para todos los colores de esa talla) y la
  lista de variantes con su estado (final, provisional o sin foto) y su versión, que cambia cuando
  cambia la foto. En la descripción, `{n}` es el número de flores de la fila del Excel: lo pone el chat.
- `fotos.csv` y `fichas.csv`: lo mismo en tabla, para las columnas de fotos y fichas del Inventario
  del Excel (clave `Producto|Color|Tamano` y `Producto|Tamano`).

No se editan a mano: los genera `tools/fotos/publicar_web.py`, en el repositorio de diseño de Petal V2.

Imágenes generadas con FLUX, de Black Forest Labs.
