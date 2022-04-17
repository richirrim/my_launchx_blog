---
title: "Objetos en Vanilla Js y Cómo crealos"
date: 2022-04-09T17:54:59-05:00
description: 'Aprenderas las diferentes y retorcidas formas de crear objetos en JS.'
image: ''
draft: false
---
## *⚠️Contenido cool en construcción...*

📦 La forma más simple de crear objetos en Vanilla JavaScript (JS) es utilizando la **forma literal 
"object = {...}"**. Ahora, no está de más mencionar que en Programación Orientada a Objetos (POO) la creación de clases, objetos, etc., JS lo hace a su estilo. Y muy rapidamente te darás cuenta a lo que me refiero cuando digo que "a su estilo", si continuas en este post y claro sera aun más obvio si ya has implementado ese paradigma en otros lenguajes como Python, PHP o Java.
 
Cuando se trata de POO, JS utiliza algo llamado funciones constructoras para la creación de objetos. Sí, no hay clases tradicionales pero **apartir de ES6** se nos ofrece una forma usando la palabra reseverda **class** pero no es más que syntactic sugar.


## 🚀LET´S FUCKING GO!!

Entonces, que vamos a aprender en este epico post? Veremos las diferentes sintaxis para construir objetos al estilo Vanilla JS. Y estás son:

- ⚡Objetos literales | **object = { ... }**
- ⚡ El constructor Object | **new Object( )**
- ⚡ Método estático create | **Object.create()**
- ⚡Funciones constructoras | **function Person( ) { ... }**
- ⚡Clases (syntactic sugar) | **class Person( ) { ... }**

## Creación de objetos usando la forma literal

Como se menciono al inicio del post, los **objetos literales** son una forma poco común y facil de crear objetos pero, pero antes de continuar creo que no está de más explicar lo que significa eso de **literal**.

### Literales

Los literales son esos valores que sueles almacenar en variables que tu mismo creas y tú sabes de lo que hablo porque si estás aquí significa que ya has recorrido un largo camino hacia el mundo de JS y ya has creado muchas variables a las que seguramente ya le has asignado valores como numbers, strings, booleanos, etc.

Así que, sí, Plebe, esos son los valores literales, pero veamos unos ejemplos rápidos.

#### Literales de tipo cadena (string) 
Un literal de tipo string es una cadena de caracteres, un texto, que está entre de comillas.

```js
const kindOfEyes = 'mangekyou sharingan' // con comillas simples o
const name = "Itachi" // con comillas dobles.
```
#### Literales de tipo número (number) 
Un literal de tipo número, son números que puedes expresar: En decimales (base 10), Hexadecimales (base 16), Octales (base 8) y Binarios (base 2).

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
Ahora, sí, veamos que es un objeto literal. Se podría resumir en que es una lista para agrupar información. Un objeto literal esta formado por elementos **par clave-valor** encerrados entre llaves **{ ... }**.
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
## Creación de objetos vacios usando el constructor Object
Antes de ir directo al grano es importante mencionar que JavaScript tiene algunos constructores incorporados, incluidos los siguientes:

```js
var soyUnObjetoVacio = new Object(); 
var soyUnTexto = new String('Bob')
var soyUnNumero = new Number(25);
var soyUnBooleano = new Boolean(true);
``` 
Y de todos ellos el único que nos interesa, obviamente, es **new Object()** constructor. El constructor **Object** crea un objeto vacío, un envoltorio. El sig. Ejemplo, almacena un objeto vacío **Object** en *itachi*.
### Cración del objeto
```javascript
let itachi = new Object();
console.log(itachi) // Output: {}
```

Ya si quieres agregarle propidades y métodos has lo sig.
```JS
itachi.name = 'Itachi Uchiha';
itachi.info = function () {
    return `Nombre del shinobbi: ${this.name}`
}

console.log(itachi) // Output: { name: 'Itachi Uchiha', info: ƒ () }
console.log(itachi.info()) // Output: 'Nombre del shinobbi: Itachi Uchiha'
```


## Creación de objetos usando una función constructura

Una función constructora podríamos decir que es la forma que JS tiene para representar **clases** y luego a partir de dicha función crear objetos usando el **operador new**.  
```JS
function Ninja() { } //  Función constructora.
const naruto = new Ninja()
console.log(naruto) // Output: Ninja {}
``` 
Y sí, a simple vista pareciera que estamos tratando con una función nombrada de toda la vida, pero la clave esta cuando mandamos a llamar a dicha función usando la palabra clave ```new```. En el momento que nosotros ponemos el operado **new** antes de la invocación de dicha función se vuelve una función constructora que nos permite crear o instanciar nuevos objetos.

> ⚡Tip: Una buena práctica es que siempre que quieras implementar una función constructora para crear objetos, el nombre de dicha función siempre debe iniciar con mayúsculas.
```js 
    // ❌ Bad 
    function ninja( ) { ... }
    function person() { ... } 
    function car( ) { ... }
    
    // ✔️Good
    function Ninja( ) { ... }
    function Person() { ... } 
    function Car( ) { ... }
```