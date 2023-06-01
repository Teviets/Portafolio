# Portafolio
<p align="center">
    <img src="./portafolio/src/assets/img/logo.png"/>
</p>

## Introduccion

En este proyecto se realizo un portafolio con los proyectos y laboratorios favoritos, y se demuestran los conocimientos que se adquirieron en la clase de sistemas y tecnologias web. A lo largo del curso se aprendieron diversas tecnologias en las que se podrian aplicar en diversos campos de la carrera de ingenieria en sistemas

## Feautures

<ul>
    <li>
        <img src="./portafolio/src/assets/img/svelte.png" style= "width: 30px; height: auto;"/> Svelte
        <br>Framework centrado en la utilizacion de componentes
    </li>
    <li>
        <img src="./portafolio/src/assets/vector/styles.svg" style= "width: 30px; height: auto;"/> CSS
        <br>Se utilizo para poder personalizar componentes de svelte
    </li>
    <li>
        <img src="./portafolio/src/assets/vector/vite.svg" style= "width: 30px; height: auto;"/> Vite
        <br>Me sirvio para comprimir los archivos JS, HTML y SCSS
    </li>
    <li>
        <img src="./portafolio/src/assets/img/firebase.png" style= "width: 30px; height: auto;"/> Firebase
        <br>Sirve para hacer host al proyecto
    </li>
<ul>

## Enlace publicado

https://proyecto-3-6445a.web.app/

## Getting start

1. Clonar repositorio `https://github.com/Teviets/Portafolio`
2. Moverse al directorio: `cd portafolio`.<br />
3. Correr `npm install` para instalar dependencias.<br />
4. Correr `npm run dev` para ver la página.

## Estructura

- `Portafolio` carpeta donde se encuentra la configuracion (package.json, vite y svelte)
- - `src` carpeta donde se encuentra los archivos .svelte .js y .css
- - - `assets` carpeta donde se encuentran las fuentes, imagenes y vectores
- - - `componentes` carpeta donde se encuentran los componentes del proyecto
- - - `App.svelte` archivo donde se reciben los componentes del proyecto
- - - `main.js` archivo donde se realiza la navegación de la página
- - `index.html` archivo donde se recibe el script de la página

## Estructura de svelte

### Codigo general de componente en Vue

```
<etiqueta a retornar>
  <!--
    Estructura visual del component
  -->
</etiqueta a retornar>

<script>

</script>

<style>
    /**
      Aplicar estilos aqui
    */
</style>
```

## Estructura de index.js

```
import './app.css'
import App from './App.svelte'

const app = new App({
  target: document.getElementById('app'),
})

export default app
```