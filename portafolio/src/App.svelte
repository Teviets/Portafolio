<script>
  import Header from './componentes/header.svelte'
  import Home from './componentes/home.svelte'
  import Acerca from './componentes/acerca.svelte'
  import Inicios from './componentes/inicios.svelte'
  import Proyectos from './componentes/proyectos.svelte'
  import AOS from 'aos';
  import 'aos/dist/aos.css';

  AOS.init();
</script>

<main>
  <div id="MiHeader">
    <Header />
  </div>
  <div id="home" >
    <Home />
  </div>
  <div id="Acerca" >
    <Acerca />
  </div>
  <div id="inicios" >
    <Inicios />
  </div>
  <div id="Proyectos" >
    <Proyectos/>
  </div>
</main>


<style>
  main{
    width: 100%;
    height: 100%;
  }
  #MiHeader{
    position: sticky;
    top: 0;
  }
  #home{
    width: 100%;
    height: auto;
  }
  #Acerca{
    width: 100%;
    height: auto;
    margin-top: 725px;
    border-top: 2px solid #EAE2B7;
    border-bottom: 2px solid #EAE2B7;
  }
</style>
