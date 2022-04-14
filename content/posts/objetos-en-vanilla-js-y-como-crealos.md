---
title: "Objetos en Vanilla Js y Cómo crealos"
date: 2022-04-09T17:54:59-05:00
description: 'Aprenderas las diferentes y retorcidas formas de crear objetos en JS.'
image: ''
draft: false
---
## *⚠️Contenido cool en construcción...*

📦 La forma más simple de crear objetos en Vanilla JavaScript (JS) es usando la forma literal pero no está de más mencionar que la creación de objetos en Programación Orientada a Objetos (POO), JS lo hace a su estilo. Y muy rapidamente te darás cuenta en este post y próximos a lo que me refiero cuando digo que "a su estilo" y sera aun más obvio si ya has implementado ese paradigma en otros lenguajes como Python, PHP o Java.
 
Cuando se trata POO, JS utiliza algo llamado funciones constructoras para la creación de objetos. Sí, no hay clases tradicionales, pero existe algo llamado syntactic sugar para poder crear clases utilizando la palabra clave `class`. Así que tranqui porque todo eso lo  veremos en próximos posts. 


## 🚀LET´S FUCKING GO!!

Entonces, que vamos a aprender en este epico post? Veremos las diferentes sintaxis para construir objetos al estilo Vanilla JS. Y estás son:

- ⚡Objetos literales (literal objects)
- ⚡Object
- ⚡Object.create()
- ⚡Funciones constructoras
- ⚡Clases (class syntactic sugar)

## Creación de objetos usando la forma literal

Dentro de esta lista de como  crear objetos de diferentes formas, los **objetos literales** son los más fáciles, rápidos de construir y usar. Y antes de continuar, creo que no está de más explicar lo que significa eso de **literal**, además de ser un **mecanismo que no todos los lenguajes poseen**.

### Literales

Los literales no son más que valores que tú vas a almacenar en las  variables que creas y tú sabes de lo que hablo porque si ya llegaste hasta esta parte de los objetos significa que has tenido un largo recorrido por el mundo de JS y ya has creado muchas variables a las que seguramente ya le has asignado valores como numbers, strings, booleanos, etc.

Así que, sí, Plebe, esos son los valores literales, pero veamos unos ejemplos rápidos.

#### Literales de tipo cadena (string) 
Un literal de tipo string es una cadena de caracteres, un texto, que está entre de comillas.

```js
const kindOfEyes = 'mangekyou sharingan' // con comillas simples o
const name = "Itachi" // con comillas dobles.
```
#### Literales de tipo número (number) 
Un literal de tipo número se pueden expresar: En decimales (base 10), Hexadecimales (base 16), Octales (base 8) y Binarios (base 2).

```js
const age = 26 
const Pisito = 3.1416
```

#### Literales de tipo Boleanos (boolean)
Un literal de tipo boolean solo tiene dos tipos de valores *true* y *false*.
```js
const isActivate = true 
const canFly = false
```

#### Literales de tipo Objeto (object)
Ahora, sí, veamos que es un objeto literal, se podría resumir en que es una lista para agrupar información que contiene elementos **par clave-valor** encerrados entre corchetes **{ ... }**.
```js
const ninja = {
    name: 'Obito', // Elmento par clave: valor
    lastname: 'Uchiha', // o propiedad par clave: valor.
    kekkeiGenkai: 'sharingan', // par clave: valor
    age: 31, // par clave: valor
    info: function () { // o métodos par clave: valor.
        return `
            Nombre: ${this.name + ' ' + this.lastname}
            Kekkei Genkai: ${this.kekkeiGenkai}
            Edad: ${this.age}
        `
    }
}
```

El término “literal” uno de sus significados es “Que reproduce exactamente lo que se ha dicho o se ha escrito “.
## Creación de objetos vacios usando el constructor Object()
new Object() crea un objeto vacío, un envoltorio.
### Cración del objeto
```javascript
let ninjaItachi = new Object();
```

### Agregando propiedades al objeto vacío.
```JS
ninjaItachi.name = 'Itachi Uchiha';
ninjaItachi.clan = 'Uchiha';
ninjaItachi.currentAge = 21;
ninjaItachi.isAlive = false
ninjaItachi.skillsUnique = []
```

### Agregando métodos
```JS
ninjaItachi.info = function () {
    return `
        NINJA, ${this.name.toUpperCase()}
        ${'------'.repeat(5)}
        Clan: ${this.clan}
        Edad Actual: ${this.currentAge}
        Habilidades unicas: ${this.skillsUnique.length ? this.skillsUnique.join(' | ') : 'Nope'}
    `
}
console.log(ninjaItachi.info())
```


## Creación de objetos usando una función constructura 
```JS
function ninjaNaruto() {
    this.name = 'Naruto Uzumaki'
    this.clan = 'Uzumaki'
    this.currentAge = '32'
    this.isAlive = true
    this.skillsUnique = ['Detección de sentimiento negativos', 'Flotar', 'Regeneración']

    this.info = function () {
       
        return `
            NINJA, ${this.name.toUpperCase()}
            ${'------'.repeat(5)}
            Clan: ${this.clan}
            Edad Actual: ${this.currentAge}
            Habilidades unicas: ${this.skillsUnique.length ? this.skillsUnique.join(' | ') : 'Nope'}
        `
    }
}
const naruto = new ninjaNaruto()
console.log(naruto.info())
``` 
