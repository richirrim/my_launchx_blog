---
title: "Objetos en Vanilla Js y cómo crealos"
date: 2022-04-09T17:54:59-05:00
description: 'Aplicando POO al estilo Vanilla JS.'
image: ''
draft: false
---

Antes de empezar es necesario mencionar que **Vanilla JavaScript (JS) no es un lenguaje basado 
en clases** pero claro que podemos implementar la programación orientada a objetos (POO). JS es un poco rebelde y no le gusta hacer las cosas como a sus demás compañeros, por ende, la forma de implementar POO en este lenguaje no es igual  a tu lenguaje favorito Orientado a Objetos. JS trabaja de una manera muy peculiar y a su manera implementa POO usando algo llamado *Prototipos* y para las *clases* usa algo llamado *funciones constructuras* pero tranki que todo lo miraremos con mucha calma para que quede claro.

JS es un lenguaje **Orientado a Objetos basado en Prototypes** y no en 
clases como en otros lenguajes. 

⚠️Contenido cool en construcción...

Ojo 👀, un constructor es una forma especial que crea o unicializa un objeto, es 
la versión de JavaScript de una clase. En JavaScript, se llama a un constructor 
cuando se crea un objeto usando la new palabra clave.

En otras palabras, el operador new utilizado junto a una función de JavaScript es 
lo que nos permite obtener un objeto constructor o función 
constructora.

## Creación de objetos vacios usando el constructor Object()
new Object() crea un objeto vacío, un envoltorio.
### Cración del objeto
```JS
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

## Creación de objetos usando la forma literal 