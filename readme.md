# Parcial Diseño Web 3
Universidad ORT, Julio 2023 - Miguel Vallvé

## Introducción
Dos amigas que comparten una pasión deciden arriesgarse y comenzar un pequeño negocio local de venta de plantas. 
Tu decides sumarte como socio tecnológico y por lo tanto tienes a cargo toda la presencia online de Plantón. 

Luego de haber analizado opciones, deciden presentar el proyecto a Fondo Verde para obtener financiación. Dentro de las bases, se requiere un sitio web modelo funcionando que muestre las principales funcionalidades. 

El equipo decide levantar rápidamente un sitio en WordPress utilizando el tema Astra (theme) que viene con contenido de prueba bastante completo. 

## Levantar Local - 1pts
Utilizar planton.zip para levantar un sitio local utilizando local by flywheel.

## Tema Hijo - 1pts
Instalar y activar el tema hijo planton-child. 
Hacer los cambios pertinentes para que WordPress te reconozca como autor del tema hijo. Cambiar la versión del tema hijo a 1.0.1

## Node - 1pts
Inicializar node dentro del tema hijo para que se genere el archivo package.json. Nombrar el paquete (package name) planton-node, establecer la versión del paquete en 0.0.1 y asignarse la autoría.

## Sass - 4pts
Incorporar `sass` al tema hijo de tal manera que se pueda trabajar en más de un archivo parcial y el resultado compilado remplace al archivo `style.css` en la raíz del tema. 

Crear dos scripts:
```js 
 `npm run sass` compila style.css. 
 `npm run sass-w` observa (watch) los cambios *.scss y compila style.css con cada cambio guardado.
```

## Bootstrap - 4pts
Agregar `Bootstrap` a través de `Node Package Manager` como una dependencia de desarrollo. Al generarse `style.css` debería incluir el css de bootstrap. Tomar en cuenta que no vamos a utilizar funcionalidades que requieran `javascript` por lo que no es necesario agregar `bootstap.min.js` al tema. Tampoco será necesario incluir los siguientes archivos parciales de `Bootstrap`

```html
_modal.scss
_toasts.scss
_forms.scss
_progress.scss
_popover.scss
```

## Colores del branding - 2pts
Cambiar los colores por defecto de `Bootstrap` por los del branding de Plantón

``` scss
$primary: #08565c;
$secondary: #025823;
```

## Integrar las Variables - 2pts
Para integrar el sistema de colores de `Bootstrap` con el tema `Astra`, debemos reemplazar las variables de `css` que el tema establece en la raíz. 

```scss
:root {
    --ast-global-color-0: #{$primary};
    --ast-global-color-1: #{$secondary};
}
```
ver [Muestra-Primary.png](/Muestra-Primary.png)

## Agregar Favicon - 1pt
Utilizar el archivo `planton-ico.png` como el ícono del sitio (favicon)

## Home - 12pts
Para presentar el sitio en el fondo, vamos a al menos dejar traducida la home y hacer algunos cambios.

-   Eliminar `Home` del menú principal y traducir a español los ítems visibles. 

-   Traducir los 3 ítems debajo del `hero` y cambiar el ícono de Free Shipping por uno de un camión.

-   Traducir los siguientes 3 ítems. Eliminar la `Llamada a la acción` (CTA) y agregar un cuarto elemento que tenga por título `Flores Para Cada Estación`. 


## Blog - 10pts
El sitio actual no tiene un blog y es una funcionalidad que queremos presentar ya que vamos a realizar una estrategia de `Inbound Marketing`. 

- Crea una página nueva llamada `Plantips` y asígnala como la página de entradas o blog.

- Crea dos `Entradas` (posts) utilizando contenido de otro blog como [craftinggeek](https://craftingeek.me/trucos-para-cuidar-flores/) o [interflora](https://www.interflora.es/blog/las-plantas-en-primavera-cuidados-basicos/)

- Cambia el layout de `/plantips` para que muestre los artículos en 1 columna para teléfonos, 2 columnas para tablets y 3 columnas para monitores grandes utilizando clases de bootstrap. Se recomienda revisar los archivos `content-blog.php`, `class-astra-loop.php`. [Ver Muestra-Blog](Muestra-Blog.png)

Tome en consideración la clases de como:

```css
.justify-content-around 
.row
.col-3
.col-lg-4
.container
```

- No permitir que los usuarios puedan dejar comentarios en ninguna `entrada` (post)

- Agregar la `barra lateral` (sidebar) en las `entradas` (posts) y eliminar `Recent Comments` de la misma. [Ver Muestra-Post](Muestra-Post.png).

## Agregar nueva categoría de productos- 3pts
Actualmente hay 2 categorías de productos: Plantas y Cactus. Agregar una tercera categoría llamada "Flores". Agregar la categoría nueva al menú junto con las otras dos.

## Agregar productos - 6pts
Agregar dos flores (productos) y asignarle la categoría "Flores" previamente creada. Se recomienda tomar el contenido y precios de otro sitio como [Uruguay Tapices](https://uruguaytapices.com.uy/producto/ramo-10-rosas-pink/)


## Footer - 2pts
En la primera columna, Cambiar el texto "Simply Natural" por "Síguenos" y centrar con el logo de Plantón. 

En la última columna cambiar el título por "Apoyos", eliminar el texto y agregar debajo el logo de Fondo Verde tomándolo de [su sitio web](https://www.fondoverde.org/)


## Créditos luego del Footer - 2pt
Cambiar "Copyright © 2023 parcial-dw3-2023" por "Copyright © 2023 Plantón"
Cambiar "Powered by parcial-dw3-2023" por "Powered by Nombre Apellido - N° Estudiante" 
# parcial_dw3_2023
