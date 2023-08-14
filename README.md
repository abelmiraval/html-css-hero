# Hero UI

## Entendiendo la composición de un archivo HTML
En que idioma esta la pagina, en este caso esta en ingles.
```html
 <html lang="en">
```

En la etiqueta head va toda la configuracion de metadatos, que haran una configuracion global de la pagina.
```html
 <head></head>
```

## ¿Qué contiene la etiqueta head de mi HTML?
Es la codificacion de caracteres que vamos a tener en nuestro sitio web, UTF-8 para agregar  Ñ, tildes.
```html
<meta charset="UTF-8">
```

Es una etiqueta para configurar el viewpoert, el viewport es el area visible del navegador.
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

## La tecnica del Wrapper
Considerar las fronteras del diseño(contenedor, wrapper), siempre tenemos que tener nuestra frontera un tamaño maximo y en base a ello programar, se recomienda centrar el wrapper.

Poner las cosas en  un contenedor, el contenedor se tiene que distribuir en muchos lugares, no podemos asumir que solo sera una pantalla.

Algunos breakpoints mas usados:
- 320, 400, 768, 1024, 1240, 1366, 1440, 1920


## Uso basico de figma
- Para poder ver los margenes, padding, usamos command + click(seleccionar el elemento).

## Creación de archivo CSS, y uso personalizado de fuentes
Podemos crear variable de fuentes, se recomienda que en una pagina web solo haiga hasta maximo 2 tipos de fuentes.

## Escribiendo nuestras primeras etiquetas HTML y estilos css del proyecto
Para crear nuestro componentes tenemos que seguir la regla de oro.
```
.hero => componente
 .wrapper => wrapper
  .hero-content => contenido
```

## Importando las imágenes en el HTML

Podemo usar esto para que no se desborda la imagen.

```css
.wrapper {
  overflow: hidden;
}
```
O podemos decir que la imagen tome el 100% de su contenedor.

```css
img {
  max-inline-size: 100%;
}
```

## Creación del botón y ancho máximo del contenedor
El contenedor del contenido debe tener un ancho máximo.

## Usando flexbox para alineacion
En flexbox no existe vertical ni horizontal, lo que existe es eje principal y el eje transversal.

El elemento que quiero hacer una alineado vertical tiene que tener un alto, asi para que se pueda alinear verticalmente.

La propiedad align-items alinea en el eje transversal, esta mal dicho que alinea en el eje vertical.

```css
.hero-content{
  display:flex;
  flex-direction: column;
  block-size: 768px;
  align-items:center;
}
```


## Usando una imagen como background
Por defecto las imagenes tienen un background-repeat y background-position, tenemos que sobreescribir dichas propiedades.

## Posiciones y apilamiento en CSS
Para poder dividir el contenido uno a lado del otro, haremos uso de la propiedad position para controlar su posición y la propiedad z-index para trabajar con el apilamiento de los elementos.

Por defecto los elementos tienen position:static, para poder usar z-index tenemos que cambiar el position por cualquier u otro valor (relative, sticky, absolute), tambien nos permite usar los insets, top, bottom, left, rigth.

## Clip-path en CSS para hacer recortes - Parte 1

<code>clip-path: polygon(0 0, 100% 0, 100% 80%, 0 100%)</code>

El punto 0,0 sera en la parte superior (x,y).

El punto 100%, 0 esto quiere decir 100% en x y 0 en y.

El punto 100%, 80%, me mantengo en la parte inferior y bajo 80%.

El punto 0, 100%, 0 por ciento en el ejex y 100% en el eje y.

## Optimización de imágenes

Las imagenes svg son mas livianas ya que pesan menos, tienen mayor rendimiento de descarga.

Los svg son para iconos, pensan menos y la imagen es perfecta, usan conjuntos matematicos para poder crearlos.

Recursos para optimizar las imagenes sin perder calidad:

[https://tinypng.com/](https://tinypng.com/)

Nos permite comprimir la imagen y tambien cambiar el tipo de archivo: jpg, webp avif. Las webp y avif son formatos con menor peso sin perder calidad de la imagen.

https://squoosh.app/

## Atributo loading para la carga de imágenes

Siguiendo con la optimización de nuestro sitio, este atributo loading de html con el valor lazy, nos permite mejorar el rendimiento que tendrá nuestra página web ya que cargara el recurso de la imagen según se vaya requiriendo, por lo que la primera carga del sitio será más rápida y por ende, optimizada.

El lazy loading va hacer efecto simpre y cuando las imagenes estan lejos del viewport, a medida que vamos haciendo scroll
las imagenes se iran cargando.

Otra tecnica seria usar Intersection Observer.

```html
    <img src="./images/vector-1.png" loading="lazy" alt="">
    <img src="./images/vector-2.svg" loading="lazy" alt="">
```

## Entendiendo el apilamiento de CSS
Ya sea que estemos trabajando con una posición diferente a static o trabajemos con un display de flex, vamos a tener acceso a modificar el apilamiento que tienen los elementos en el eje z (hay más formas de obtener acceso a dicho apilamiento).

Tener en cuenta tambien el orden de apilamiento de los elementos, conforme se vayan agregando se iran apilando.


[Stack content css](https://developer.mozilla.org/es/docs/Web/CSS/CSS_positioned_layout/Understanding_z-index/Stacking_context)
