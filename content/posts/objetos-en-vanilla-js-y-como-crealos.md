---
title: "Objetos en Vanilla Js y Cómo crealos"
date: 2022-04-09T17:54:59-05:00
description: 'Aprenderas las diferentes y retorcidas formas de crear objetos en JS.'
image: ''
draft: false
---

📦 La forma más simple de crear objetos en Vanilla JavaScript (JS) es usando la forma literal pero no está de más mencionar que la creación de objetos en Programación Orientada a Objetos (POO), JS lo hace a su estilo. Y muy rapidamente te darás cuenta en este post y próximos a lo que me refiero cuando digo que "a su estilo" y sera aun más obvio si ya has implementado ese paradigma en otros lenguajes como Python, PHP o Java.
 
Cuando se trata POO, JS utiliza algo llamado funciones constructoras para la creación de objetos. Sí, no hay clases tradicionales, pero existe algo llamado syntactic sugar para poder crear clases utilizando la palabra clave `class`. Así que tranqui porque todo eso lo  veremos en próximos posts. 


## 🚀LET´S FUCKING GO!!

Entonces, que vamos a aprender en este epico post? Veremos las diferentes sintaxis para construir objetos al estilo Vanilla JS. Y estás son:
- Objetos literales (literal objects)
- Object
- Object.create()
- Funciones constructoras
- Clases (class syntactic sugar)

## Creación de objetos usando la forma literal
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

⚠️Contenido cool en construcción...