<script>
import CardProyect from './card.svelte'

import Airbnb from '../assets/img/airbnb.png'
import TableTrek from '../assets/img/tabletrek.png'
</script>

<div id="contenedorProyecto">
    <h2>Proyectos</h2>
    <CardProyect 
                nameProyect="Copia de Airbnb" 
                img={Airbnb}
                description="En este proyecto, consistio en realizar una copia de la pagina de airbnb, en la cual se utilizo html, css y javascript, para poder realizar la pagina. El framework que se utilizo fue React, el cual es un framework que permite realizar aplicaciones web de una manera mas rapida y eficiente, este framework este centrado en la utilizacion de componentes."
                link="https://copiaairbnb.web.app/"
                width="1000px"
                height="550px"
    />
    <CardProyect 
                nameProyect="Table trek" 
                img={TableTrek}
                description="En este proyecto, consistio en realizar un proyecto libre. Con mis compañeros decidimos hacer una aplicacion donde se gestionen reservas de restaurantes y se pueden gestionar usuario y eliminar las diversas reservaciones en los restaurantes. Para realizar este proyecto se utilizo el framework Vue.js, este framework esta centrano en la utilizacion de componentes, y es muy parecido a React."
                link="http://18.220.61.52/"
                width="1000px"
                height="550px"
    />
</div>

<style>
#contenedorProyecto{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}
</style>