<script >
import CardsCarousel from './CardsCarousel.vue'

export default{
    components: {
        CardsCarousel
    }
}
</script>
<template>
    <div class="container-one-s">
        <div class="bg-color">
            <div class="cont-content container">
                <h1>NUESTROS SERVICIOS</h1>
                <img class="arrow" src="../img/downArrow.png">
            </div>
        </div>
    </div>
    <CardsCarousel></CardsCarousel>
    <div class="container-two-s container">
        <h2 >NUESTRA METODOLOGÍA DE TRABAJO</h2>
        <div style="width: 100px; border-bottom: 3px solid #F26800; margin: auto;"></div>
        <h3 class="cts-subtitle-two">Para mantener la efectividad en nuestro trabajo y la satisfacción del cliente, nos regimos y trabajamos de la siguiente manera:</h3>
        <div>
            <div class="c5-flex c5-ld">
                <h4>Proyecto <img class="icons-c2" src="../img/projectsIcon.png"></h4>
                <p>En primera instancia, cuando nos contacten vamos a agendar una reunión, de tal manera que nos puedan comunicar qué quieren que realicemos para el sitio o aplicación web. Por supuesto, incluyendo nuestra ayuda y guía para tener una idea más completa. Una vez completado eso, se empieza el desarrollo del trabajo según lo deseado.</p>
                <h4>Tiempo<img class="icons-c2" src="../img/timerIcon.png"></h4>
                <p>El tiempo va a variar según la dificultad del proyecto. Para un sitio web informativo la duración del trabajo puede ser alrededor de un mes. Caso contrario de ser un trabajo más grande o una aplicación, lo hablaremos cuando se reunan con nosotros.</p>
                <h4>Precios<img class="icons-c2" src="../img/pricesIcon.png"></h4>
                <p>Con mucho gusto le brindaremos toda la información necesaria y detallada, a fin de que pueda conocer en profundidad nuestros servicios, y los costos asociados a los mismos. En este sentido, nuestros profesionales altamente capacitados estarán disponibles para atender sus requerimientos y ofrecer soluciones a medida. No dude en ponerse en contacto con nosotros para que podamos ayudarlo a alcanzar sus objetivos con el mejor servicio posible.</p>
            </div>
            <div class="c5-flex">
                <h4>Contrato<img class="icons-c2" src="../img/contractIcon.png"></h4>
                <p>Todos los lineamientos del trabajo serán escritos mediante un contrato (duración del proyecto, método de pago, soporte, tecnologías utilizadas, entre otras aclaraciónes) para confianza y seguridad de la empresa y el cliente. De dicho contrato se tendrá una copia para ambas partes.</p>
                <h4>Garantía <img class="icons-c2" src="../img/guaranteeIcon.png"></h4>
                <p>Una vez finalizado el proyecto, otorgamos daremos mes y medio de garantía del trabajo, esto quiere decir que si nos necesitan durante ese lapso para corregir algún error o cualquier sitación disponible, vamos a estar para resolverlo sin ningún costo adicional.</p>
                <h4>Soporte<img class="icons-c2" src="../img/support2Icon.png"></h4>
                <p>Una vez terminada la garantía, pueden volver a contactarnos ya sea para un nuevo cambio, cosas nuevas que quieran agrrgar al trabajo o cualquier otro motivo. En este caso dicho soporte tiene un costo adicional.</p>
            </div>
        </div>
    </div>
</template>
<style scoped>

.container-one-s{
    background-image: url(../img/bgOne-services.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    background-position: bottom;
    height: 500px;
}
.bg-color{
    background-color: rgba(0, 0, 0, 0.671);
    height: 100%;
    display: grid;
    place-items: center;
}
.cont-content{
    text-align: center;
    color: white;
}
.cont-content h1{
    font-weight: bold;
}
.arrow{
    margin-top: 30px;
}
.container-two-s{
    text-align: center;
    width: 100%;
    margin-bottom: 30px;
}
.container-two-s p{
    color: rgb(68, 68, 68);
}
.container-two-s h2{
    margin-top: 30px;
    font-weight: bold;
}
.container-two-s h2{
    text-align: center;
}
.container-two-s h4{
    font-weight: bold;
}
.cts-subtitle-two{
    margin: 30px 0 30px 0;
}
.c5-flex{
    display: inline-block;
    width: 45%;
    padding: 20px;
    text-align: justify;
    box-shadow: 0px 0px 14px -11px rgba(0,0,0,1);
-webkit-box-shadow: 0px 0px 14px -11px rgba(0,0,0,1);
-moz-box-shadow: 0px 0px 14px -11px rgba(0,0,0,1);
}

.icons-c2{
    width: 35px;
    margin-left: 10px;
}

@media screen and (max-width: 1000px) {
    .c5-flex{
        display: inline-block;
        width: 90%;
        padding: 20px;
        text-align: justify;
        box-shadow: 0px 0px 14px -11px rgba(0,0,0,1);
        -webkit-box-shadow: 0px 0px 14px -11px rgba(0,0,0,1);
        -moz-box-shadow: 0px 0px 14px -11px rgba(0,0,0,1);
    }
}

</style>