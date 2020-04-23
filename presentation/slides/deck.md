---
marp: true
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.jpg')
---

![bg left:40% 80%](https://upload.wikimedia.org/wikipedia/commons/9/91/Electron_Software_Framework_Logo.svg)

# **Electron JS**

Build cross-platform desktop apps with JavaScript, HTML, and CSS

---

# What is electron

- Chromium :heart: 
- Nodejs :+1:

<div class="mermaid">
graph TB
    Electron --> NodeJs
    Electron --> Chromium
    NodeJs   --> FileSystem
    NodeJs   --> CompileModule
    NodeJs   --> CommonJs
    Chromium --> Render/css/html
    Chromium --> WebApi
    Chromium --> DOM
</div>

<!-- 
Electron:
electron es un sistema runtime osea provee un ambiente para crear aplicaciones de escriotrio con html5, css y javascript. Es un proyecto opensource que comenzo en github con la idea de crear un editor de texto multiplataforma construido apartir de tecnologias web (Atom), electron combina el modulo de contenido de chromium y nodejs runtime para permitirle a los desarrolladores construir paginas web e interactuar con el sistema operativo.

Chromium: 
es la vesion opensource del navegador web de google con algunas pequeñas deferencias, el content module es el core que permite renderizar una pagina web.

Nodejs:
es el lenguaje backend en javascript (v8 engine) que nos permite comunicarnos con el sistema operativo a partir de sus modulos
 -->

---

# Who is using Electron

- Github (*atom*)
- facebook (*nuclide*)
- slack
- discord
- nylas (*mail client*)
- brave (*browser*)
- microsoft (*vscode*) :cupid:

---

# How does electron works


<div class="mermaid">
graph LR
    MainProcess-->RenderProcess1
    MainProcess-->RenderProcess2
    MainProcess-->RenderProcessN
</div>

<!-- 
Main process:
nodejs - server side
es el encargado del ciclo de vida de los eventos como el inicio, salida, preparacion entre otros, ademas de estar encargado de la comunicacion con el sistema operativo por medio de sus APIS.

Render process: 
instancia de chromim - cliente side
pueden cargar paginas web (html, css, js), ya que pueden ser multiples procesos toma todas las ventajas de chromium multiprocess, a diferencia de las paginas web que conocemos existe la posibilidad de acceder directamente al api de node desde el proceso render
 -->
---


<!-- mermaid.js -->
<script src="https://unpkg.com/mermaid@8.1.0/dist/mermaid.min.js"></script>
<script>mermaid.initialize({startOnLoad:true});</script>
