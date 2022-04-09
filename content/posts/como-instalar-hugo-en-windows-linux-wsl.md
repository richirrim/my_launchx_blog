---
title: "Cómo instalar Hugo en Windows"
date: 2022-04-08
description: 'Quieres aprender a instalar Hugo? este es tu post👊🤠.'
image: images/launchx.png
draft: false
---

Hugo es un fast Framework para crear sitios web estáticos y está hecho en Go! . Ojo, para usarlo no necesitas instalar Go!, tranqui, ntp, no es necesario la instalación. Con su increíble velocidad y flexibilidad, Hugo hace que la construcción de sitios web sea divertida nuevamente.

Hugo lo puedes instalar en los sig. Sistemas Operativos:
- macOs
- Windows
- Linux
- OpenBSD
- FreeBSD 

Y en cualquier otra PC donde se pueda instalar y ejecutar sin problemas Go!.

## *Let´s Fucking Go!*

### Instalando Hugo con un .exe (Instalación fast)

Solo tienes que descargar el instalador sin importar si estás en Windows, Mac o Linux y será todo. Lo puedes descargar desde el sig. enlace la versión  adecuada para tu plataforma desde [Hugo.exe](https://github.com/gohugoio/hugo/releases).

Ojito, se recomienda que lo instales o mejor, que descomprimas el **.zip**  en algún lugar de tu PATH para facilitar su uso. 

Ahora nos dirigimos a nuestro disco local `C:\` para crear un par de carpetas que se recomiendan para descomprimir los archivos de Hugo y así poder tener acceso a él desde cualquier terminal del S.O.

Una vez en `C:\` crearás una nueva carpeta llamada *Hugo* y dentro dos más, una llamada `bin` y otra `site` y sería todo. Dentro de la carpeta `bin` descomprimiremos los archivos del zip descargado.  Y la carpeta `sites`las puedes utilizar, si quieres, para guardar tus proyectos construidos con Hugo.

Ahora dirígete a tu terminal y teclas el comando `hugo version`, el cual te devolverá la versión y así sabrás que todo ha ido good.

### Instalando Hugo desde la terminal de Windows usando Chocolatey

    choco install hugo -confirm

Y sí, una vez termine la instalación para verificar que todo está correcto, usa el comando `hugo version`, si te devuelve la versión todo bien. Ahora ya está todo listo para empezar a utilizar comandos como `hugo server` desde la consola.

### Instalando Hugo desde la terminal de Windows usando Ubuntu WSL

Este proceso es un poco más lento, pero es otra manera de instalar Hugo en tu S.O.

⚠️ Construyendo steps...