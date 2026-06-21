# Lección: Introducción a CSS y Hojas de Estilo

## Intro

> En la lección anterior construiste una página con HTML: pusiste encabezados, párrafos, listas e imágenes. Tu página funciona perfectamente, pero, seamos honestos, todavía se ve bastante sencilla. ¡Hoy cambiamos eso! CSS es el lenguaje que le da color, estilo y personalidad a todo lo que ves en internet. Si HTML son los cimientos y las paredes de un edificio, CSS es la pintura, los muebles y la decoración. Al final de esta lección habrás transformado una página de gimnasio aburrida en algo que se ve profesional de verdad. ¡Empecemos!

## Desarrollo

### ¿Qué es CSS?

> CSS significa Hojas de Estilo en Cascada (*Cascading Style Sheets*). La palabra "cascada" es clave. Significa que los estilos fluyen desde reglas generales hasta reglas más específicas, como el agua cayendo por niveles.
>
> CSS trabaja junto con HTML, pero son archivos separados y hablan lenguajes distintos. HTML te dice *qué* hay en la página. CSS te dice *cómo* se ve. Esta separación es una de las mejores prácticas del desarrollo web moderno. Mantiene tu código ordenado y fácil de modificar. ¿Quieres cambiar todos los colores de tu sitio web? Solo editas el archivo CSS sin tocar para nada el HTML.

### Herramientas de trabajo: CodePen

> Aquí está nuestra herramienta para esta lección: CodePen. Es un editor en línea completamente gratuito. No necesitas crear una cuenta ni descargar nada. Simplemente abres el enlace y ya puedes programar. 
>
> Verás tres paneles: HTML, CSS y, abajo, una pantalla que se actualiza en tiempo real mientras escribes. Esto es exactamente lo que usamos los desarrolladores web para hacer prototipos rápidos.
>
> Para esta clase usaremos la página de nuestro gimnasio ficticio: "Gym Pro". Tiene un encabezado, un párrafo y una lista; todo en un HTML que ya conoces de la lección anterior. Pero si miras la vista previa, verás texto negro sobre fondo blanco: sin carácter y sin energía. CSS va a cambiar eso completamente.

### ¿Cómo conectar CSS con HTML?

> Antes de escribir cualquier estilo, necesitas decirle al navegador que existe un archivo CSS. Hay dos formas principales para hacerlo:
>
> 1. **CSS Interno:** Escribes las reglas dentro de una etiqueta `<style>` directamente en el archivo HTML. Es útil para pruebas rápidas.
> 2. **CSS Externo (La mejor práctica):** Creas un archivo separado con la extensión `.css` y lo vinculas usando una etiqueta `<link>` dentro de la sección `<head>` de tu HTML.
>
> En CodePen esto ya está resuelto automáticamente: lo que escribas en el panel CSS se aplica al HTML de forma inmediata. En proyectos reales siempre usarás el archivo externo porque separar el estilo del contenido hace que tu código sea mucho más limpio y fácil de mantener.

### Estructura de una regla CSS

> Cada bloque de CSS tiene siempre la misma estructura:
>
> * **Selector:** Le dice a CSS a qué elemento HTML vas a darle estilo.
> * **Llaves `{ }`:** Abren y cierran el bloque de código.
> * **Declaraciones:** Van dentro de las llaves. Cada una tiene una **propiedad** (¿qué quieres cambiar?) y un **valor** (¿cómo quieres que quede?), separados por dos puntos (`:`) y terminados con un punto y coma (`;`).
>
> Una regla CSS es tan simple como esto:
> ```css
> body {
>   background-color: orange;
> }
> ```
> Nunca olvides el punto y coma (`;`) al final de cada declaración. Es el error más común de los principiantes.

### Los 3 selectores fundamentales

> Vamos a ver los tres tipos de selectores que más usarás en tus proyectos:
>
> 1. **Selector de Etiqueta:** Es el más directo. Escribes el nombre de cualquier etiqueta HTML y los estilos se aplican a todos los elementos de ese tipo en la página. Por ejemplo, al aplicar al `<body>` un fondo oscuro azul marino y texto claro, toda la página cambia de golpe. Si pones el `<h1>` en naranja, el nombre del gimnasio resaltará de inmediato. Su única limitación es que afecta a todos los elementos por igual: si tuvieras tres etiquetas `<h1>`, las tres se verían idénticas.
> 2. **Selector de Clase:** Una clase es una etiqueta reutilizable que tú mismo inventas. La añades en el HTML con el atributo `class="..."` y en CSS la seleccionas escribiendo un punto (`.`) antes del nombre. Por ejemplo, si tienes dos párrafos y al primero le asignas la clase `class="eslogan"`, en CSS puedes escribir `.eslogan` para darle un tamaño de letra grande, letra cursiva y color amarillo. El segundo párrafo no cambiará porque no tiene esa clase. Puedes usar una clase en muchos elementos diferentes.
> 3. **Selector de ID:** Un ID es un identificador único. Solo puede existir un elemento con ese ID en toda la página. En HTML lo agregas con el atributo `id="..."` y en CSS lo seleccionas con el símbolo de numeral o gato (`#`) antes del nombre. Lo usamos para cosas únicas, como un menú de navegación o la sección de servicios. Por ejemplo, `#servicios` puede dar un fondo azul oscuro, un borde naranja a la izquierda y un espaciado interno (*padding*).

### Propiedades clave: Tipografía y el Modelo de Caja

> Vamos con tres propiedades que usarás siempre:
>
> * **Tipografía (`font-family`):** Define qué tipo de letra usa el texto. Fuentes como Arial o sans-serif son opciones seguras que existen en todos los navegadores.
> * **El Espaciado (`margin` y `padding`):** Piensa en una caja de regalo. El **padding** es el papel de burbujas de adentro: el espacio entre el contenido real y los bordes de la caja. El **margin** es el espacio vacío alrededor de la caja entera, el cual la separa de los demás objetos. 
> 
> Al poner `margin: 0;` en el `<body>`, eliminamos el espacio en blanco que los navegadores añaden por defecto. Al poner un `padding: 20px;`, le damos aire al contenido para que no esté pegado a los bordes de la pantalla.

### El resultado final

> Al unir todo, verás cómo cada regla trabaja en equipo:
> * El `body` establece la base con fondo oscuro y su tipografía.
> * El `<h1>` usa el naranja característico de "Gym Pro".
> * La clase `.eslogan` hace que el lema se vea con más energía.
> * El ID `#servicios` crea una sección visualmente separada.
> * Un selector compuesto como `#servicios li` le aplica un margen inferior a cada elemento de la lista para que respiren y no queden amontonados.
> 
> ¡Pasamos de una página en blanco a un diseño con carácter usando solo unas 18 líneas de CSS!

### Tres errores muy frecuentes en CSS

> Antes de practicar, recuerda cuidar estos detalles:
> 1. **Olvidar el punto y coma (`;`):** Si te falta al final de una declaración, el estilo simplemente no se aplicará.
> 2. **Olvidar el punto (`.`) en las clases:** Si no lo pones en el archivo CSS, el navegador no encontrará tu clase.
> 3. **Olvidar el numeral (`#`) en los ID:** Si no lo colocas antes del nombre, el estilo no funcionará.

## Cierre

> Resumiendo: hoy aprendiste a conectar CSS con tu HTML, a usar los tres selectores fundamentales (etiqueta, clase e ID) y a aplicar propiedades clave de color, tipografía y espaciado.
>
> En la descripción del video encontrarás el enlace a CodePen con todo el código listo. Ábrelo, cambia los colores por los que más te gusten, modifica la tipografía y ajusta el padding. ¡Es tu página, hazla tuya! En la siguiente lección combinarás todo lo que sabes para construir una página de perfil personal completa. ¡Nos vemos ahí!
