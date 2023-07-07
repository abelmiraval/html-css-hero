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
