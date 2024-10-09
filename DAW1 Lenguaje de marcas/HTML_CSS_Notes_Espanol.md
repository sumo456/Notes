
# HTML5 vs Otras Versiones

## DOCTYPE
- La declaración <!DOCTYPE> debe ser la primera en un documento HTML, antes de la etiqueta <html>.
- Es una instrucción para el navegador sobre la versión de HTML en la que está escrita la página.
- HTML5 no requiere una referencia a un DTD (Definición de Tipo de Documento), a diferencia de HTML 4.01, que se basa en SGML.
- Siempre incluya la declaración <!DOCTYPE> para los documentos HTML, para que el navegador sepa qué tipo de documento esperar.

## Metadatos en HTML5
- La etiqueta `<meta>` proporciona metadatos sobre el documento HTML. No se muestran en la página, pero pueden ser procesados por las máquinas.
- HTML5 tiene un nuevo atributo, `charset`, que facilita la definición del conjunto de caracteres: `<meta charset="UTF-8">`.
- La etiqueta `<meta>` en HTML5 no requiere una etiqueta de cierre, a diferencia de XHTML.

## Nuevos Elementos Semánticos en HTML5
- Nuevos elementos semánticos como:
    - `<header>`: especifica encabezados de un documento o sección.
    - `<nav>`: define un conjunto de enlaces de navegación.
    - `<footer>`: especifica uno o más pies de página.
    - `<article>`: especifica contenido independiente y autónomo (ej. una publicación en un foro, un artículo de periódico).
    - `<section>`: agrupa contenido temáticamente relacionado.
    - `<aside>`: contenido al margen del contenido principal, típicamente en una barra lateral.

## Elementos Multimedia en HTML5
- Los elementos `<audio>` y `<video>` permiten incrustar audio y video sin necesidad de Flash:
```html
<audio controls>
  <source src="audio.mp3" type="audio/mpeg">
  <source src="audio.ogg" type="audio/ogg">
</audio>
```

# Estructura y Etiquetas HTML

## Estructura de la Página
- La estructura básica de una página HTML incluye:
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Título de la Página</title>
  </head>
  <body>
    <h1>Mi Primer Encabezado</h1>
    <p>Mi primer párrafo.</p>
  </body>
</html>
```
- Todos los documentos HTML constan de dos partes principales:
  - Head: Contiene los metadatos y está encerrado entre las etiquetas <head>.
  - Body: Contiene el contenido visible y está encerrado entre las etiquetas <body>.

## Elementos Block y Inline
- **Elementos Block**:
  - Ejemplos: `<div>`, `<p>`, `<section>`.
  - Comienzan en una nueva línea y ocupan todo el ancho disponible.
  - Usados comúnmente para la estructura y el diseño.
  
- **Elementos Inline**:
  - Ejemplos: `<span>`, `<a>`, `<img>`.
  - No comienzan en una nueva línea y solo ocupan el espacio necesario.

# Fundamentos de CSS

## Posicionamiento en CSS
- CSS tiene varios métodos de posicionamiento para controlar cómo aparecen los elementos en la página:
  - `static`: Posicionamiento predeterminado. Los elementos aparecen en el flujo normal.
  - `relative`: Posicionado en relación con su posición normal, utilizando las propiedades top, bottom, left, o right.
  - `absolute`: Posicionado en relación con el ancestro posicionado más cercano.
  - `fixed`: Posicionado en relación con la ventana de visualización, se queda en el mismo lugar aunque la página se desplace.
  - `sticky`: Cambia entre posicionamiento relativo y fijo dependiendo del desplazamiento.

## Propiedad Display
- `display: block`: Los elementos se apilan verticalmente y ocupan todo el ancho.
- `display: inline`: Los elementos se colocan en línea con otros y no interrumpen la línea.
- `display: inline-block`: Combina características de block e inline, permitiendo aplicar ancho y alto pero permaneciendo en línea.
- `display: none`: Oculta el elemento del diseño de la página.

# Especificidad e Herencia en CSS

## Especificidad
- La especificidad determina qué reglas CSS son aplicadas por el navegador cuando múltiples reglas pueden aplicarse al mismo elemento.
- La jerarquía de especificidad se calcula en función del número de IDs, clases y elementos usados en el selector.
- Ejemplo de cálculo de especificidad:
  - `#id` (100 puntos) > `.clase` (10 puntos) > `elemento` (1 punto)

## Herencia
- Algunas propiedades en CSS son heredadas por los elementos secundarios (ej., font-family, color).
- Propiedades como `background-color` no se heredan por defecto.
- La herencia ayuda a reducir la redundancia en CSS aplicando un estilo al elemento padre, que se pasa a los hijos.

# Flexbox y Grid Layout

## Flexbox
- Flexbox proporciona una forma más eficiente de alinear y distribuir el espacio entre los elementos de un contenedor.
- Propiedades como `justify-content`, `align-items`, y `flex-direction` controlan el diseño.
- Ejemplo para centrar contenido:
```css
#container {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

## CSS Grid
- CSS Grid permite crear diseños web complejos usando filas y columnas.
- Las propiedades `grid-template-columns` y `grid-template-rows` definen la estructura de la cuadrícula.
- Ejemplo para crear una cuadrícula de 3 columnas:
```css
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
```

# Formularios HTML

## Elementos de Formulario
- Los formularios HTML recogen la entrada del usuario.
- Los elementos comunes del formulario incluyen:
  - `<input>`: Define controles de entrada (texto, email, contraseña, etc.).
  - `<textarea>`: Entrada de texto de varias líneas.
  - `<button>`: Envía el formulario.
  
## Tipos de Entrada en HTML5
- HTML5 introdujo nuevos tipos de entrada como:
  - `type="email"`: Valida el formato de correo electrónico.
  - `type="number"`: Acepta entrada numérica.
  - `type="range"`: Entrada deslizante.
  - `type="date"`: Selector de fecha.

---

Este es un resumen de alto nivel de los temas clave cubiertos en los documentos que proporcionaste. Cada sección explica conceptos fundamentales de HTML y CSS, incluyendo características modernas como Flexbox, CSS Grid y nuevas etiquetas semánticas en HTML5.
