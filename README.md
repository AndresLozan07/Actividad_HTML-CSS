# Papelería Centauros

Página web hecha con HTML y CSS por Andrés Felipe Lozano Ramirez.

## Sobre el proyecto

Papelería Centauros es una papelería de barrio ficticia ubicada en Bucaramanga. En la página se muestran algunos productos escolares, sus precios y la información que pueden necesitar estudiantes, padres y profesores.

La idea es que las personas puedan conocer la papelería y revisar los productos desde el computador o el celular.

## Archivos del proyecto

```text
papeleria-centauros/
├── index.html
├── segunda-pagina.html
├── README.md
├── css/
│   └── styles.css
├── images/
├── video/
└── capturas/
```

- `index.html`: tiene la presentación de la papelería, los productos y otra información.
- `segunda-pagina.html`: tiene los precios y un formulario para los pedidos.
- `css/styles.css`: contiene los estilos de las páginas.
- `images/`: carpeta para las imágenes.
- `capturas/`: guarda las imágenes de cómo se ve la página.

## Diseño de la página

Usé un fondo oscuro con colores como azul, cian y violeta para que la página tuviera un estilo moderno. También usé diferentes tamaños de espacios y fuentes para organizar el contenido.

## Especificidad en CSS

La especificidad sirve para saber qué estilo se aplica cuando dos reglas quieren cambiar el mismo elemento.

Por ejemplo, para los enlaces del menú:

```css
a {
    color: var(--cian);
}

.menu__lista a {
    color: var(--texto);
}
```

En este caso se aplica el color de `.menu__lista a`, porque su selector tiene más especificidad.

También hice pruebas con los precios de los productos y con las filas de la tabla para ver qué estilo se aplica cuando hay varias reglas.

## Herencia

La propiedad `font-family` está en `body`, así que los textos de la página pueden usar esa fuente sin tener que escribirla en cada elemento.

En cambio, el borde de una tarjeta no se aplica automáticamente a los textos que están dentro de ella.

## Modelo de cajas

En CSS, el tamaño de un elemento también puede incluir el espacio interno (`padding`) y los bordes.

En el caso de `.opinion`, el ancho máximo del contenido es de 576 px. Al sumar 48 px de `padding` y 4 px de borde, el ancho total es de 628 px.

Los márgenes de dos elementos seguidos también pueden juntarse. En ese caso, dos márgenes de `1rem` pueden terminar dejando un espacio de `1rem`.

## Selectores

Usé `:nth-child(even)` para seleccionar las filas pares de la tabla de precios. En este caso, se aplica a las filas 2, 4 y 6 del cuerpo de la tabla.

## Vista en celular

Usé `@media (max-width: 600px)` para adaptar la página a pantallas pequeñas.

- El menú se organiza en una sola columna.
- Las tarjetas de productos ocupan el ancho disponible.
- Se reducen algunos espacios y tamaños para que el contenido se vea mejor.
