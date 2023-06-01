<script>
    import Logo from '../assets/img/logo.png'
    function scrollToHome() {
        const scrollTarget = document.getElementById('home');
        scrollTarget.scrollIntoView({ behavior: 'smooth' });
    }
    function scrollToAcerca(){
        const scrollTarget = document.getElementById('Acerca');
        scrollTarget.scrollIntoView({ behavior: 'smooth' });
    }
    function scrollToIniciosFront(){
        const scrollTarget = document.getElementById('inicios');
        scrollTarget.scrollIntoView({ behavior: 'smooth' });
    }
    function scrollToProyectos(){
        const scrollTarget = document.getElementById('Proyectos');
        scrollTarget.scrollIntoView({ behavior: 'smooth' });
    }

</script>

<div id="miHeader">
    <div id="btnHome">
        <button id="identificador" on:click={scrollToHome} data-aos="fade-right">
            <img id="miLogoWi"src={Logo} alt="" width="50">
            <h3 style="color: #EAE2B7;">Sebastian Estrada</h3>
        </button>
    </div>
    <nav id="navigationTop" data-aos="fade-left">
        <button class="navBtn" on:click={scrollToAcerca}>Acerca de mi</button>
        <button class="navBtn" on:click={scrollToIniciosFront}>Inicios frontend</button>
        <button class="navBtn" on:click={scrollToProyectos}>Proyectos</button>
    </nav>
</div>

<style>
    #miHeader{
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        border-bottom: 1px solid #EAE2B7;
        background-color: #003049;
    }
    #btnHome{
        display: flex;
        align-items: center;
    }
    #identificador{
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        gap: 10px;
        align-items: center;
        background-color: transparent;
        border: none;
        color: #EAE2B7;
    }
    #miLogoWi{
        border-radius: 50%;
    }
    nav{
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        margin-top: 20px;
        margin-right: 10px;
        margin-bottom: 10px;
        gap: 10px;
    }

    .navBtn {
        background: transparent; /* color de fondo */
        color: #F77F00; /* color de fuente */
        border: 2px solid #F77F00; /* tamaño y color de borde */
        padding: 16px 20px;
        border-radius: 3px; /* redondear bordes */
        position: relative;
        z-index: 1;
        overflow: hidden;
        display: inline-block;
    }
    .navBtn:hover {
        color: #EAE2B7;/* color de fuente hover */
    }
    .navBtn::after {
        content: "";
        background: #F77F00; /* color de fondo hover */
        position: absolute;
        z-index: -1;
        padding: 16px 20px;
        display: block;
        left: -20%;
        right: -20%;
        top: 0;
        bottom: 0;
        transform: skewX(-45deg) scale(0, 1);
        transition: all 0.3s ease;
    }
    .navBtn:hover::after {
        transition: all 0.3s ease-out;
        transform: skewX(-45deg) scale(1, 1);
    }

    @media screen and (max-width: 1020px){
        #navigationTop{
            display: none;
        }
        #btnHome{
            width: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
        }
    }
</style>
