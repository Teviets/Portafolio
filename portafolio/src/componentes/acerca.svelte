<script>
import Presentacion from '../assets/img/presentacion.jpg'

</script>

<div id="componenteAcerca">
    <h2>Acerca de mi</h2>
    <div id="contenido">
        <div id="principal">
            <div id="miIMG">
                <img src={Presentacion} alt="" width="300px" data-aos="fade-up-right">
            </div>
            <div id="texto">
                Soy Sebastian Estrada Tuch de 20 años, estudiante de tercer año de Ingeniería en
                Ciencias de Computación y Tecnología de la Información de la Universidad del Valle de
                Guatemala. Esta carrera universitaria me llamó la atención desde pequeño por el gusto
                que tengo por los videojuegos y su funcionamiento. Mi familia está integrada por mis
                padres y dos hermanas, yo ocupo el tercer lugar entre los tres; nos gusta compartir
                momentos de familia, así como nuestras dificultades y logros. Algunos de mis hobbies,
                además de los videojuegos, son los deportes, en los que me gusta participar, siendo el
                principal el fútbol, asimismo, disfruto invirtiendo tiempo de calidad con mis amigos y
                familia, y ser autodidacta en el aprendizaje de nuevas tecnologías de programación.
            </div>
        </div>
       <div id="contacto">
            <h2 id="titCont">Contacto</h2>
            <div id="contactos" data-aos="fade-up">
                <button class="btnContacto">
                    <a href="https://github.com/Teviets" target="_blank">
                        <img src="https://img.icons8.com/ios-filled/50/000000/github.png"/>
                    </a>
                </button>
                <button class="btnContacto">
                    <a href="https://codepen.io/Teviets" target="_blank">
                        <img src="https://img.icons8.com/ios-filled/50/000000/codepen.png"/>
                    </a>
                </button>
                <button class="btnContacto">
                    <a href="https://www.instagram.com/sebasest37/" target="_blank">
                        <img src="https://img.icons8.com/ios-filled/50/000000/instagram.png"/>
                    </a>
                </button>
            </div>
       </div>
    </div>
</div>

<style>
#componenteAcerca{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
}
#contenido{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-top: 50px;
    margin-bottom: 50px;
}
#principal{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    gap: 10px;
    margin-left: 150px;
    margin-right: 150px;
    margin-top: 25px;
}
#texto{
    width: 50%;
    text-align: justify;
}
#miIMG{
    margin-left: 50px;
}
#contacto{
    margin-top: 35px;
    gap: 35px;
}
#contactos{
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    width: 100%;
}
.btnContacto{
    border: none;
    background-color: transparent;
}
#titCont{
    margin-left: 30px;
}

@media screen and (max-width: 1020px){
    #componenteAcerca{
        width: 100%;
    }
    #principal{
        flex-direction: column;
        justify-content: center;
        align-items: center;
        margin-left: 0px;
        margin-right: 0px;
    }
    #texto{
        width: 100%;
        text-align: justify;
    }
    #miIMG{
        margin-left: 0px;
    }
    #contacto{
        margin-top: 35px;
        gap: 35px;
    }
    #contactos{
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        width: 100%;
    }
    #titCont{
        margin-left: 30px;
    }
}
</style>