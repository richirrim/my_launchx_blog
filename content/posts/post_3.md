---
title: "Html | Buenas prácticas"
date: 2022-04-07
description: 'Conjunto de buenas practicas para ecribir codigo html más limpio, consistente y ordenado.'
---
📷 [Instagram | Ricardo Ortega](https://www.instagram.com/richirrim/) para encontrar más contenido.

Recuerden que muchas de estas convenciones su uso o como la usen va depender de la empresa en la que estés trabajando, el proyecto, el equipo, etc. Y como dije antes su uso puede variar de proyecto en proyecto. Esta es una pequeña guia, es solo una probadita del clean code, así que ya puedes empezar a cosntruir proyectos más limpios, consistentes y escalables 👊🤠.

## Buenas practicas de accesibilidad

Los siguientes atributos no modifican en nada el resultado final que se mostrara en el navegador, pero para él al navegador le importa y mucho que los uses por temas de accesibilidad y además es una buena práctica usarlos.

Es decir, no son utilizados solo para darle más información o semántica al navegador, también hay que tener en cuenta que hay usuarios que sufren algún tipo de discapacidad auditiva o visual y estos utilizan navegadores especiales y gracias a los atributos como `alt` ayudaras a los usuarios con alguna discapacidad a saber que su puntero está sobre una imagen y que tiene que ver con algún animal por ejemplo.


### Atributo alt=""

En este caso el contendido o el valor del `alt` debe ser una descripción breve de las imagen a mostrar.

**Example**
```html
<!-- BAD ❌ -->
<img src="/img/logo.png">

<!-- GOOD ✅ -->
<img src="/img/logo.png" alt="Soy el logo de esta web"> 
```
	
	
### Atributo title=""

El valor o contenido del atributo `title` debe ser una descripción breve de a donde lleva el enlace que tengas pensado usar en tu web.

**Example** 

```html
<!-- BAD ❌ -->
<a href="twitch.tv/ryszardriich"></a>

<!-- GOOD ✅ -->
<a href="twitch.tv/ryszardriich" 
   title="Este enlace te lleva a mi canal de twitch: ryszardriich"></a>
```
## Buenas practica de legibilidad

Este pequeño detallito de escribir todas las etiquetas en minúscula, créeme ayuda mucho a la hora de leer el html para ti y también todo tu equipo. Y si vas escribir todo en minúsculas no se te ocurra que es buena idea mezclar mayúsculas con minúsculas, porque no lo es, es mala practica.

### Etiquetas html, atributos y valores siempre en minúsculas

Obviamente si escribes mayúsculas o mezclas minúsculas con mayúsculas no veras ningún error, el navegador no se va a quejar, todo funcionara pero no esta chido hacerlo se coherente con tu código. 

Recuerda la frase `'Que puedas hacerlo, no significa que debes hacerlo o que sea correcto'`.
```html
<!-- BAD ❌ -->
<DIV CLASS="GOLAAAAAA"></DIV>

<!-- VERY, VERY BAD ❌ -->	
<DIV class="color"></DIV>
	
<!-- GOOD ✅ -->
<div clas="color"></div>
```
### Usa siempre comentarios

Es una buena practica poner comentarios para poder visualizar rápidamente las secciones de tu html y también para saber donde está cada componente.

*Example*
```html
<!---------- Header principal | Section ------------>
<header class="main-header">
  <div class="container  horizontal-align">
    <div class="horizontal-align">
      <!---------- Logo | Component --------------->
      <a class="logo-link" title="Logo de Facebook" href="/">
          <img class="logo" witdh="32" height="32" src="/images/logo-facebook.png" alt="Logo de la página">
      </a>
      <!----------- User | Component -------------->
      <div class="user>...</div>
      <button class="new-post__button">Post</button>
    </div>
  </div>
</header>
```
## Buenas practicas al usar atributos booleanos

Es una buena practica no poner el valor al hacer uso de un atributo booleano.

Atributos booleanos:
- checked
- selected
- disabled

**Example 1**
```html
<!-- BAD ❌ -->
<input type="checkbox" disabled="disabled"></input>

<!-- GOOD ✅ -->
<input type="checkbox" disabled></input>
```	
**Example 2**
```html
<!-- BAD ❌ -->
<input type="checkbox" checked="checked"></input>

<!-- GOOD ✅ -->
<input type="checkbox" checked></input>
```

## Agregar un tamaño fijo a las imagenes

Es muy buena practica siempre añadir tamaños fijo por defecto a las imagines agregando los atributos `witdh` y `hight`. Ojo, nos es necesario agregar el valor dentro de los atributos, es decir, no es necesario poner em, px, etc.

Por que? por temas de que si por alguna razón no carga la imagen, no se desmaquete el Layout. Es decir, Si no pones el tamaño fijo y la imagen no carga el espacio que ocupaba en el Layout no sera el mismo que si hubiera cargado con normalidad y, por ende, todo el layout se puede mover y no queremos eso verdad.

**Example**

```html
<!-- BAD ❌ -->
<img src="/images/barry-profile.jpg">

<!-- GOOD ✅ -->
<img src="/images/barry-profile.jpg" width="100" hight="100">
```

Les dejo algunas guías de estilo más completas:
- [Google HTML/CSS Style Guide](https://google.github.io/styleguide/htmlcssguide.html)
- [La Guía de Estilo en HTML que deberías de seguir para tener un Código Limpio](https://www.kikopalomares.com/blog/la-guia-de-estilo-en-html)


# MAY THE *DEMO EFFECT* BE WITH YOU
 Si encontraste útil este 🚀post, 🔗compártelo con todo los 👤terricolas del planeta🌎tierra y no olvides seguirme en [instagram](https://www.instagram.com/richirrim/) para más.
