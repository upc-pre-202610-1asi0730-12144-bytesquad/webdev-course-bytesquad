# Lección: Estructura Básica de HTML, Elementos y Atributos

## Intro

> En la lección anterior aprendiste algo fundamental: un sitio web está hecho de contenido, que es HTML, y de estilo, que es CSS. Hoy nos meteremos de lleno en el HTML. Vas a aprender qué son las etiquetas, qué son los elementos y qué son los atributos. Estas son las tres piezas básicas con las que se construye absolutamente cualquier página web que has visitado en toda tu vida. Al final de esta lección vas a tener tu primera página HTML completa escrita por ti mismo, funcionando en tu navegador. ¡Empecemos!

## Desarrollo

### ¿Qué es HTML?

> Empecemos con la pregunta más básica. ¿Qué es HTML? Sus siglas significan Lenguaje de Marcado de Hipertexto. La palabra clave aquí es "marcado". HTML no calcula ni decide nada, simplemente marca o etiqueta cada parte del contenido para decirle al navegador qué es cada cosa.
>
> Una etiqueta es justamente eso: una palabra envuelta entre signos de menor que y mayor que, como `<h1>` o `<p>`, que indica el tipo de contenido. 
>
> Cuando una etiqueta de apertura y una de cierre envuelven contenido en el medio, a ese conjunto completo se le llama elemento. Por ejemplo, la etiqueta de apertura `<h1>`, el texto que escribas y la etiqueta de cierre `</h1>` (con una barra inclinada) forman juntos un elemento.

### Estructura base en CodePen

> Vamos a CodePen para verlo en acción. No necesitas crear una cuenta ni instalar nada. Abres el enlace y ya puedes escribir código. En el panel HTML, toda página comienza con esta estructura base:
>
> * La etiqueta `<html>` envuelve absolutamente todo el documento.
> * Dentro va la etiqueta `<head>`, que contiene información sobre la página que no se ve directamente (como el título que aparece en la pestaña del navegador).
> * Luego va la etiqueta `<body>`, que contiene todo el contenido visible: textos, imágenes, botones y todo lo que el usuario realmente ve en pantalla. Por ahora vamos a trabajar dentro del `<body>`, que es donde vivirá casi todo nuestro contenido.

### Anidamiento y Sangría

> Antes de seguir escribiendo, fíjate en algo importante de la estructura que acabamos de ver. Los elementos pueden contener otros elementos adentro, como cajas dentro de cajas. La etiqueta `<html>` contiene a `<head>` y a `<body>`. Más adelante, el `<body>` va a contener encabezados, párrafos e imágenes. A esto se le llama anidamiento y es la base de cómo se organiza toda página web.
>
> Una buena práctica es usar sangría. Esto significa dejar espacios al inicio de cada línea para que las etiquetas que están dentro de otras se vean visualmente más adentro. Esto no cambia cómo se ve la página en el navegador, pero hace que tu código sea mucho más fácil de leer para ti y para cualquier otra persona.

### Llenando el Body: Encabezados y Párrafos

> Empecemos a llenar el `<body>` con contenido real. Primero, los encabezados. HTML tiene seis niveles, desde `<h1>` hasta `<h6>`. El `<h1>` es el título principal de la página y solo debería usarse una vez. Escribo `<h1>` con el texto "Mi página de perfil". Los siguientes niveles, como `<h2>` y `<h3>`, son para subtítulos de menor importancia o secciones adentro de la página.
>
> Ahora, el párrafo se crea con la etiqueta `<p>`. Aquí escribo un texto normal como una breve descripción sobre mí. Guardo y miro la vista previa. El `<h1>` aparece grande y en negrita por defecto, y el párrafo aparece como texto normal debajo. El navegador interpreta automáticamente esas etiquetas con un estilo básico, incluso sin que hayamos tocado CSS todavía.

### ¿Qué son los atributos?

> Si una etiqueta nos dice "qué" tipo de contenido es, ¿qué es un atributo? Un atributo es información extra sobre ese elemento, y se escribe dentro de la misma etiqueta de apertura. Un atributo siempre tiene un nombre y un valor separados por un signo igual, y el valor va entre comillas.
>
> Por ejemplo, en la etiqueta `<img>`, el atributo `src` le dice al navegador de dónde sacar la imagen. El atributo `alt` describe la imagen por si no llega a cargar o para personas que usan lectores de pantalla. Los atributos son la forma en que las etiquetas reciben información adicional para funcionar correctamente.

### Usando atributos en código real

> Vamos a usar atributos. Agrego una etiqueta `<img>` con el atributo `src` apuntando a una imagen y el atributo `alt` con la descripción "Foto de perfil". Fíjate que la etiqueta `<img>` no tiene una etiqueta de cierre separada. Se cierra a sí misma porque no envuelve ningún contenido de texto en el medio.
>
> Ahora agrego un enlace con la etiqueta `<a>`, que necesita el atributo `href` para indicar a dónde lleva ese enlace. Aquí lo apunto a una página externa. El texto que queda entre la etiqueta de apertura y cierre es lo que el usuario verá y donde podrá hacer clic. Ejecuto la vista previa: la imagen aparece en pantalla y el enlace se muestra subrayado y en azul, que es el estilo por defecto del navegador.
>
> Una etiqueta puede tener más de un atributo a la vez, separándolos con un espacio. Por ejemplo, en la misma etiqueta `<img>` podría agregar un tercer atributo llamado `width` para definir el ancho de la imagen en píxeles. El orden de los atributos dentro de la etiqueta no importa; puedes escribir `src` primero o `alt`, el resultado visual es el mismo. Lo único que importa es que cada atributo tenga su nombre, su signo igual y su valor entre comillas.

### El atributo Class

> Hay un atributo especial que vas a usar muchísimo más adelante: `class`. Por ahora, solo necesitas saber que te permite ponerle una etiqueta personalizada a un elemento, algo así como un grupo o categoría. En la siguiente lección sobre CSS vas a usar este atributo para darle estilo y color a elementos específicos. Por hoy solo recuerda que existe y que se ve así: `class="nombre-que-tú-elijas"`.

### Dos errores muy comunes en HTML

> Antes de cerrar, veamos dos errores muy comunes:
>
> 1. **Olvidar la etiqueta de cierre:** Si abres un párrafo con `<p>` pero no lo cierras con `</p>`, el navegador puede mostrar el contenido de forma desordenada porque no sabe dónde termina ese elemento.
> 2. **Olvidar las comillas en los atributos:** Si escribes el atributo `src` sin comillas, en muchos casos el navegador no entenderá dónde termina ese valor, especialmente si contiene espacios.
>
> Revisa siempre que cada etiqueta tenga su cierre y que cada atributo tenga su valor entre comillas.

## Cierre

> Resumiendo: una etiqueta marca el tipo de contenido; un elemento es la etiqueta de apertura, el contenido y la etiqueta de cierre juntos; y un atributo agrega información extra dentro de la etiqueta de apertura.
>
> Con encabezados, párrafos, imágenes y enlaces ya tienes las piezas básicas para construir cualquier página. En la descripción tienes el enlace a CodePen con el código de esta lección listo para que experimentes. En la siguiente lección vamos a añadir más elementos para que tu página empiece a tomar forma real. ¡Nos vemos ahí!