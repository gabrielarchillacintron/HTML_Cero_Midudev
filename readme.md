>[!NOTE]
>Curso de HTML desde cero de Midudev <br>
>[Youtube](www.youtube.com/@midulive) | [Video](https://youtu.be/3nYLTiY5skU)
# Indice
* [HTML (Hypertext Markup Language)](#html-hypertext-markup-language)
    * [Elementos](#elementos)
        * [Etiquetas](#etiquetas)
        * [Atributos](#atributos)
    * [Estructura basica de un documento HTML](#estructura-basica-de-un-documento-html)
    * [Semantica](#semantica)
    * [Enlaces](#enlaces)
    * [Roles](#roles)
    * [Descargas](#descargas)
    * [Formularios](#formularios)
        * [Datalist](#datalist)
        * [Details y Summary](#details-y-summary)
    * [Ventanas Emergentes](#ventanas-emergentes)
        * [Dialog](#dialog)
    * [Scripts](#scripts)
        * [Ejemplo Basico](#ejemplo-basico)
___
# HTML (Hypertext Markup Language)
* Descripcion contenido = HTML
* Presentacion = CSS
* Interactividad = JavaScript
## Elementos
Los elementos son los que contienen la <strong>informacion</strong> y se representan por <strong>etiquetas</strong>. <br>
Existen los elementos normales y tambien los reemplazables (img, input, br, hr) que no tienen contenido. <br>
Hay dos tipos de elementos:
* <strong>Elementos de bloque (block)</strong> <br>
    Ocupan todo el ancho disponible y comienzan en nueva linea. <br>
    Ejemplos: div, h1, p, ul, ol, li, section, article, header, footer, nav, main, form, table
* <strong>Elementos en linea (inline)</strong> <br>
    Solo ocupan el espacio necesario y no comienzan en nueva linea. <br>
    Ejemplos: span, a, img, input, strong, em, br, label, button
#### Etiquetas
* Titulos
    * Principal
        ```HTML
        <h1>Titulo Principal</h1>
        ```
    * h1 -> h6
* Parafos
    ```HTML
    <p>parrafo</p>
    ```
    Dentro de los elementos se pueden tener mas elementos
* Strong <br>
    Hace enfasis dentro de un parafo
    ```HTML
    <p>Texto<strong>Texto en negrita</strong>Texto</p>
    ```
* Listas
    * Desordenada
        ```HTML
        <ul>
            <li>Elemento 1</li>
            <li>Elemento 2</li>
            <li>Elemento 3</li>
        </ul>
        ```
    * Ordenada
        ```HTML
        <ol type="" reverse start="">
            <li>Elemento 1</li>
            <li>Elemento 2</li>
            <li>Elemento 3</li>
        </ol>
        ```
        * type = a (letras), A (letras mayusculas), i (numeros romanos), I (numeros romanos mayusculas), 1 (numeros)
        * reverse = true (invierte el orden)
        * start = numero (inicia la lista en el numero indicado)

        De igual manera puedes asignarle el valor a cada elemento `<li value="numero">Elemento</li>`,respetando el orden establecido de la lista al continuar desde el asignado.

#### Etiquetas Reemplazables
#### Atributos
* Imagenes <br>
    Etiquetas como esta se le conoce como <strong>reemplazables</strong> que significan que su contenido es reemplazado por el contenido de los <strong>atributos</strong> que le dan mas informacion al elemento. <br>
    Estos atributos pueden ser <strong>globales</strong> o <strong>especificos</strong> del elemento.
    ```HTML
    <img
        loading="lazy"
        hidden
        id="id"
        class="clase"
        src="url" 
        alt="texto alternativo" 
        width="ancho" 
        height="alto" 
        title="titulo">
    ```
    * loading = indica que la imagen debe cargarse de forma diferida (lazy) o de forma automatica (eager), esto ayuda a mejorar el rendimiento de la pagina
        * lazy = carga la imagen cuando esta a punto de entrar en el viewport (visible para el usuario), pero no utilizar en imagenes muy arriba de la pagina porquue puede producir un efecto de parpadeo al cargar la imagen
        * eager = carga la imagen inmediatamente
    * src = ruta de la imagen
    * alt = texto alternativo en caso de que la imagen no cargue y para  accesibilidad/SEO
    * width = ancho de la imagen
    * height = alto de la imagen
    * title = texto que aparece al pasar el mouse sobre la imagen
    * hidden = oculta la imagen
    * id = identificador unico del elemento
    * class = identificador que agrupa elementos
* Input
    ```HTML
    <input 
        type="text" 
        placeholder="texto de ayuda" 
        value="valor por defecto" 
        disabled 
        readonly 
        required
        label="etiqueta">
    ```
    * type = tipo de input (text, password, email, number, checkbox, radio, submit, etc)
    * placeholder = texto de ayuda que aparece dentro del input
    * value = valor por defecto del input
    * disabled = deshabilita el input
    * readonly = hace que el input sea de solo lectura
    * required = hace que el input sea obligatorio
    * label = etiqueta que describe el input (aparece fuera del input)
* Video
    ```HTML
    <video 
        src="url-del-video" 
        width="ancho" 
        height="alto" 
        controls 
        autoplay
        loop 
        muted 
        poster="url-de-la-imagen">
    </video>
    ```
    * src = ruta del video
    * width = ancho del video
    * height = alto del video
    * controls = muestra los controles del video (play, pause, volume, etc)
    * autoplay = reproduce el video automaticamente
    * loop = reproduce el video en bucle
    * muted = silencia el video
    * poster = imagen que se muestra antes de reproducir el video
* Audio
    ```HTML
    <audio 
        src="url-del-audio" 
        controls 
        autoplay
        loop 
        muted>
    </audio>
    ```
    * src = ruta del audio
    * controls = muestra los controles del audio (play, pause, volume, etc)
    * autoplay = reproduce el audio automaticamente
    * loop = reproduce el audio en bucle
    * muted = silencia el audio

    La apariencia de los controles depende del navegador y del sistema operativo.
* iFrame
    ```HTML
    <iframe 
        src="url" 
        width="ancho" 
        height="alto" 
        title="titulo" 
        frameborder="0" 
        allow="fullscreen; accelerometer; picture-in-picture"
        allowfullscreen
        loading="lazy">
    </iframe>
    ```
    El elemento `<iframe>` (inline frame) se utiliza para incrustar otro documento HTML dentro del documento actual. <br>
    No se puede hacer con cualquier pagina web ya sea por el servidor o por la misma pagina web que lo impida con los metadatos. <br>
    * src = ruta del contenido a mostrar
    * width = ancho del iframe
    * height = alto del iframe
    * title = titulo del iframe (importante para accesibilidad)
    * frameborder = borde del iframe (0 = sin borde, 1 = con borde)
    * allow = permisos parav el contenido del iframe
    * allowfullscreen = permite que el iframe se muestre en pantalla completa
    * loading = indica que el iframe debe cargarse de forma diferida (lazy) o de forma automatica (eager), esto ayuda a mejorar el rendimiento de la pagina
        * lazy = carga el iframe cuando esta a punto de entrar en el viewport (visible para el usuario), pero no utilizar en iframes muy arriba de la pagina porquue puede producir un efecto de parpadeo al cargar el iframe
        * eager = carga el iframe inmediatamente

>[!WARNING]
>Cuidado con los allow ya que pueden ser un riesgo de seguridad si se permite todo. Es mejor especificar solo lo necesario.

>[!NOTE]
>Existen paginas como [MDN Web Docs](https://developer.mozilla.org/es/) donde se puede consultar la documentacion de las etiquetas y sus atributos.
>Para el caso de las imagenes, videos y iframes se recomienda utilizar `style="width:100%; aspect-ratio:radio de la imagen/video;"` para que >sean responsive y mantengan la relacion de aspecto de la propia imagen/video.

>[!IMPORTANT]
>Los navegadores tienen <strong>user agent stylesheets</strong> que son estilos por defecto que aplican a las etiquetas. Por esta razon se creo el <strong>css reset</strong> que elimina estos estilos por defecto. De igual manera se pueden <strong>sobreescribir</strong> estos estilos.

## Estructura basica de un documento HTML
```HTML
<!DOCTYPE html>
<html lang="es">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width">
        <title>Titulo de la pagina</title>
        <meta name="description" content="Descripcion de la pagina">
        <meta property="og:title" content="Titulo de la pagina">
        <meta property="og:description" content="Descripcion de la pagina">
        <meta property="og:image" content="url-de-la-imagen">
        <meta property="og:image-alt" content="Texto alternativo de la imagen">
        <link rel="alternate" hreflang="es" href="url-de-la-pagina-en-espanol">
        <link rel="canonical" href="url-de-la-pagina-canonical">
        <meta name="robots" content="index, follow">
        <link rel="icon" href="favicon.ico" type="image/x-icon">
        <style></style>
    </head>
    <body>
        <h1>Hola Mundo</h1>
        <p>Mi primer pagina web</p>
    </body>
</html>
```
* `DOCTYPE html` = declara el tipo de documento
* `html lang="es"` = elemento raiz del documento y el atributo lang indica el idioma
* `head` = contiene metadatos y enlaces a recursos externos <br>
* `meta charset="UTF-8"` = define la codificacion de caracteres
* `meta name="viewport" content="width=device-width"` = hace que la pagina sea responsive y ocupe todo el ancho del dispositivo
* `title` = titulo de la pagina que aparece en la pestaña del navegador
* `meta name="description" content="Descripcion de la pagina"` = descripcion de la pagina que aparece en los resultados de busqueda
* `meta property="og:title" content="Titulo de la pagina"` = titulo de la pagina para redes sociales
* `meta property="og:description" content="Descripcion de la pagina"` = descripcion de la pagina para redes sociales
* `meta property="og:image" content="url-de-la-imagen"` = imagen de la pagina para redes sociales
* `meta property="og:image-alt" content="Texto alternativo de la imagen"` = texto alternativo de la imagen para redes sociales
* `link rel="alternate" hreflang="es" href="url-de-la-pagina-en-espanol"` = enlace a la version en otro idioma de la pagina
* `link rel="canonical" href="url-de-la-pagina-canonical"` = enlace a la version canonica de la pagina para evitar contenido duplicado
* `meta name="robots" content="index, follow"` = indica a los motores de busqueda si deben indexar la pagina y seguir los enlaces
* `link rel="icon" href="favicon.ico" type="image/x-icon"` = enlace al icono de la pagina que aparece en la pestaña del navegador
* `style` = contiene estilos CSS internos
* `body` = contiene el contenido visible de la pagina

>[!IMPORTANT]
>Dentro del head se encuentran los metadatos que son informacion sobre la pagina web que no es visible para el usuario pero si para los motores de busqueda y navegadores. Los mencionados son algunos de los mas importantes.

## Semantica
La semantica en HTML se refiere al uso adecuado de las etiquetas para describir el contenido de la pagina web. <br>
* `section` es una seccion generica de contenido
* `article` es un contenido independiente que puede ser distribuido por si solo
* `nav` es una seccion de navegacion
* `aside` es un contenido relacionado pero no esencial.
* `header` es el encabezado de una seccion o pagina
* `footer` es el pie de pagina de una seccion o pagina
* `main` es el contenido principal de la pagina, debe ser unico en la pagina
* `div` es un contenedor generico sin significado semantico
* `span` es un contenedor en linea generico sin significado semantico
* `aside` es un contenido relacionado pero no esencial

## Enlaces
```HTML
    <a 
        href="url" 
        title="titulo" 
        target="_blank" 
        rel="noreferrer"
        > texto del enlace 
    </a>
```
Enlaza a otra pagina o recurso.
* href = url del enlace
* title = texto que aparece al pasar el mouse sobre el enlace
* target = donde se abre el enlace (por ejemplo, _blank para abrir en una nueva pestaña)
* rel = relacion entre la pagina actual y la pagina enlazada
    * noreferrer = no enviar la informacion de referencia al abrir el enlace

Enlaza a un correo electronico
```HTML
    <a href="mailto:correo@ejemplo.com">Enviar correo</a>
```
Enlaza a un numero de telefono
```HTML
    <a href="tel:+1234567890">Llamar</a>
```
Enlaza a whatsapp
```HTML
    <a href="https://wa.me/1234567890">Enviar mensaje</a>
```

## Roles
Los roles son atributos que se utilizan para mejorar la accesibilidad de la pagina web. <br>
Siempre es utilizar primeramente las etiquetas semanticas antes de usar roles. <br>
Ejemplos de uso de roles:
```HTML
    <header role="banner"></header>
    <nav role="navigation"></nav>
    <main role="main"></main>
    <aside role="complementary"></aside>
    <footer role="contentinfo"></footer>
    <section role="region" aria-labelledby="titulo"></section>
    <button role="button"></button>
```

## Descargas
```HTML
    <a download="Nombre de la imagen" href="url-del-archivo">
        <img
                id="Logo"
                class="Logo"
                width="350"
                height="200"
                src="imagenes/imagen2.gif" 
                alt="Logo" 
                title="Logo"
            >
    </a>
```
El atributo download en la etiqueta `<a>` indica que el enlace es para descargar un archivo en lugar de navegar a el. El valor del atributo download puede ser el nombre con el que se guardara el archivo. Si no se especifica, se usara el nombre del archivo en la url.

>[!WARNING]
>Solo funciona para archivos/recursos del mismo origen (misma pagina web). No funciona para enlaces externos.

## Formularios
```HTML
    <form action="url-de-envio" method="metodo-de-envio">
        <fieldset>
            <legend>Formulario de contacto</legend>
            <div>
                <label for="nombre">Nombre:</label>
                <input type="text" id="nombre" name="nombre" placeholder="Ingresa tu nombre" required>
            </div>

            <div>
                <label>Email:
                    <input type="email" name="email" placeholder="Ingresa tu email" required>
                </label>
            </div>

            <button type="submit">Enviar</button>
        </fieldset>
    </form>
```
* form = contenedor del formulario
    * action = url a la que se enviaran los datos del formulario
    * method = metodo de envio (GET, POST)
* fieldset = agrupa elementos relacionados dentro del formulario
* legend = titulo del grupo de elementos
* for = vincula el label con el input mediante el id
* placeholder = texto de ayuda que aparece dentro del input
* type = tipo de input (text, email, password, submit, tel, etc), ayuda a la validacion del formulario y la experiencia del usuario

El `div` se utiliza en este caso para apilar los elementos en bloque e igual sirve para agrupar los elementos y aplicar estilos. Lo ideal es estilarlos como `style="display:block"` u otras propiedades.
Los `button` que estan dentro de un formulario por defecto son de tipo `submit`, pero es buena practica especificarlo. <br>
Puedes definir patrones de validacion para los inputs con el atributo `pattern="expresion-regular"`.

>[!IMPORTANT]
>Ambas formas de usar label son correctas. La primera es mas accesible ya que el atributo for vincula el label con el input mediante el id mientras que la segunda forma es mas comoda ya que no es necesario usar el id y el for, pero puede ser menos accesible. Mayormente es cuestion de preferencia.

### Datalist
```HTML
    <label for="navegador">Elige tu navegador favorito:</label>
    <input list="navegadores" id="navegador" name="navegador" placeholder="Navegador">
    <datalist id="navegadores">
        <option value="Chrome">
        <option value="Firefox">
        <option value="Safari">
        <option value="Edge">
        <option value="Opera">
    </datalist>
```
El elemento `<datalist>` contiene una lista de opciones predefinidas para un elemento `<input>` asociado. El usuario puede seleccionar una de las opciones de la lista o ingresar un valor diferente. No se puede estilar el listado desplegable, es un elemento de funcionamiento simple. <br>
Existe tambien `select` pero crea una lista fija, `datalist` proporciona autocompletado.

### Details y Summary
```HTML
    <details>
        <summary>Mas informacion</summary>
        <p>Esta es la informacion adicional que se muestra al hacer clic en "Mas informacion".</p>
    </details>
```
El elemento `<details>` se utiliza para crear un widget que el usuario puede abrir y cerrar. El elemento `<summary>` define un resumen o leyenda para el contenido del `<details>`. Al hacer clic en el `<summary>`, se muestra u oculta el contenido del `<details>`.

## Ventanas Emergentes
### Dialog
```HTML
    <dialog id="miDialogo">
        <form method="dialog">
            <p>Este es un cuadro de dialogo.</p>
            <menu>
                <button value="cancel">Cancelar</button>
                <button value="confirm">Confirmar</button>
            </menu>
        </form>
    </dialog>

    <button onclick="document.getElementById('miDialogo').showModal();">Abrir Dialogo</button>
    <button onclick="document.getElementById('miDialogo').close();">Cerrar Dialogo</button>
```
El elemento `<dialog>` representa un cuadro de dialogo o ventana emergente. <br>
Proporciona una forma nativa y semántica de crear modales sin depender tanto de JavaScript complejo o bibliotecas externas. <br>

### Scripts
```HTML
    <script src="script.js" defer></script>
```
* src = ruta del archivo JavaScript
* defer = indica que el script debe ejecutarse despues de que el documento haya sido parseado

#### Ejemplo Basico
```HTML
    <dialog id="dialogo">
        <h1>Dialogo</h1>
        <p>Este es un cuadro de dialogo.</p>
        <button id="cerrar">Cerrar</button>
    </dialog>

    <button id="abrir">Abrir Dialogo</button>

    <script>
        window.abrir.addEventListener(click, () => {
            window.dialogo.showModal();
        })
        window.cerrar.addEventListener(click, () => {
            window.dialogo.close();
        })
    </script>

