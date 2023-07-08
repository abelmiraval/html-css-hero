# Hero UI

## Entendiendo la composición de un archivo HTML
En que idioma esta la pagina, en este caso esta en ingles
```html
 <html lang="en">
```

En la etiqueta head va toda la configuracion de metadatos, que haran una configuracion global de la pagina
```html
 <head></head>
```

## ¿Qué contiene la etiqueta head de mi HTML?
Es la codificacion de caracteres que vamos a tener en nuestro sitio web, UTF-8 para agregar  Ñ, tildes
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
- Para poder ver los margenes, padding, usamos command + click(seleccionar el elemento)

## Creación de archivo CSS, y uso personalizado de fuentes
Podemos crear variable de fuentes, se recomienda que en una pagina web solo haiga hasta maximo 2 tipos de fuentes.

## Escribiendo nuestras primeras etiquetas HTML y estilos css del proyecto
Para crear nuestro componentes tenemos que seguir la regla de oro
```
.hero => componente
 .wrapper => wrapper
  .hero-content => contenido
```

## Importando las imágenes en el HTML

Podemo usar esto para que no se desborda la imagen.

```
.wrapper {
  overflow: hidden;
}
```
O podemos decir que la imagen tome el 100% de su contenedor

```
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

<pre>
  .here-content{
    display:flex;
    flex-direction: column;
    block-size: 768px;
    align-items:center;
  }
</pre>


## Usando una imagen como background
Por defecto las imagenes tienen un background-repeat y background-position, tenemos que sobreescribir dichas propiedades

## Posiciones y apilamiento en CSS
Para poder dividir el contenido uno a lado del otro, haremos uso de la propiedad position para controlar su posición y la propiedad z-index para trabajar con el apilamiento de los elementos

Por defecto los elementos tienen position:static, para poder usar z-index tenemos que cambiar el position por cualquier u otro valor (relative, sticky, absolute), tambien nos permite usar los insets, top, bottom, left, rigth.

## Clip-path en CSS para hacer recortes - Parte 1

<pre>clip-path: polygon(0 0, 100% 0, 100% 80%, 0 100%)</pre>

El punto 0,0 sera en la parte superior (x,y)

El punto 100%, 0 esto quiere decir 100% en x y 0 en y.

El punto 100%, 80%, me mantengo en la parte inferior y bajo 80%

El punto 0, 100%, 0 por ciento en el ejex y 100% en el eje y
