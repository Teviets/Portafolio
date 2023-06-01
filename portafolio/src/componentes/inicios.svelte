<script>
import CardLabs from './card.svelte';

import Servidor from '../assets/img/servidor.png'
import CSS from '../assets/img/css.png'
import Chat from '../assets/img/chat.png'
import Memoria from '../assets/img/memoria.png'
</script>

<div id="IniciosContainer">
    <h1>Laboratorios</h1>
    <div id="cardsContainerInicio">
        <div class="item">
            <CardLabs 
                nameProyect="Configurando un servidor" 
                img={Servidor}
                description="En este laboratorio se configuro un servidor con el sistema operativo Ubuntu Server 20.04 LTS, se configura el acceso remoto desde Windows 10. Esto es fue impactante para mi pues descubri un gusto por la utilizacion de cloud computing y me impulso a querer conocer mas sobre AWS."
                link="#"
                width="600"
                height="300"
                />
        </div>
        <div class="item">
            <CardLabs 
                nameProyect="Estilos CSS" 
                img={CSS}
                description="Este laboratorio consistio en realizar una copia de un diseño hecho con css de una pagina especifica y buscar implementar estilos un poco mas avanzados, en este laboratorio aprendimos la utiliza de @media y como poder hacer trancisiones desde css."
                link="https://css-stw.web.app/"
                width="600"
                height="300"
                />
        </div>
        <div class="item">
            <CardLabs 
                nameProyect="Javascript" 
                img={Chat}
                description="En este laboratorio aprendiamos sobre la utilizacion de javascript y de la potencia que tiene este lenguaje de programacion, llegamos diseñar nuestro propio chat de la clase, haciendo un fetch a una instancia en mongo diseñada por el catedratico. Tambien llegamos a diseñar la pagina completamente desde javascript."
                link="https://chatstw.web.app/"
                width="600"
                height="300"
                />
        </div>
        <div class="item">
            <CardLabs 
                nameProyect="Memoria React" 
                img={Memoria}
                description="En este laboratorio implementamos el framework React con webpack, para poder diseñar un juego de memoria, en el cual se utilizo diversas librerias que facilitaron de gran manera la creacion de los diversos componente y permitiendo que estos sean reactivos a lo que usuario esta empleando en el juego."
                link="https://lab-8-fd228.web.app/"
                width="600"
                height="300"
                />
        </div>
    </div>
</div>

<style>
    #cardsContainerInicio {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-template-rows: repeat(2, 1fr);
        gap: 10px;
    }

    .item {
        background-color: transparent;
        padding: 10px;
    }
</style>