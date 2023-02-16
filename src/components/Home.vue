<script >
</script>
<template>

    <div class="bg-one">
        <div style="background-color: rgba(0, 0, 0, 0.616);">
            <div class="container container-one">
                <h1 class="c1-title">Si necesitas un sitio web para tu empresa</h1>
                <h2 class="c1-p1">Este es el lugar correcto</h2>
                <h2 class="c1-p2">Bienvenido a<span style="font-weight: bold"> Art Development</span></h2>
                <h2 class="c1-p3">Expandiendo la calidad</h2>
                <a href="https://msng.link/o/?artdevelopment__=ig" target="_blank"><button class="orange-btn" role="link">CONOCE SOBRE NOSOTROS</button></a>
            </div>
        </div>
    </div>

    <div class="container container-two">
        <h2 class="c2-title">Proyectos hechos con creatividad</h2>
        <div style="width: 100px; border-bottom: 3px solid #F26800; margin-bottom: 15px;"></div>
        <div class="c2-flex">
            <div class="c2-project-content">
                <h4>Con qué te ayudaremos?</h4>
                <p>En nuestro servicio, realizamos programación de alta calidad, de tal manera que el sitio tenga la temática deseada por el cliente, incluyendo disponibilidad del sistema en distintos dispositivos.</p>
                <p>También, nos enfocamos en realizar detalladamente lo solicitado por nuestro cliente, de manera que se cumpla la satisfacción de el mismo. Si aún no sabes bien lo que quieres, no te preocupes, nosotros te vamos a ayudar a descubrirlo!</p>
                <RouterLink 
                class="nav-link" 
                active-class="active-link" 
                exact-active-class="exact-active-link" 
                aria-current="page" 
                to="/contact"><button class="orange-btn">CONTACTANOS</button></RouterLink>
            </div>
            <div class="c2-project-content-img">
                <img class="c2-img-creativity" src="../img/creativity.jpg">
            </div>
        </div>
    </div>

    <div class="container-three" style="">
        <div class="container">
            <h4>Sin preocupaciones por el mantenimeinto de tu sitio</h4>
            <div style="width: 200px; border-bottom: 3px solid #F26800; margin: auto;"></div>
            <p>Además de desarrollar tu sitio web ideal, nuestro compromiso va a otro nivel! Dandote mes y medio de garantía para el producto, en caso de que nos necesites, aquí vamos a estar. Por supuesto, vamos a estar siempre atentos para cuando requieran de nuestros servicios, ofreciendo el mismo nivel de calidad, profesionalismo y compromiso.</p>
            <RouterLink 
            class="nav-link" 
            active-class="active-link" 
            exact-active-class="exact-active-link" 
            aria-current="page" 
            to="/services"><button class=" btn-services">NUESTROS SERVICIOS</button></RouterLink>
        </div>
    </div>

    <div class="container-four">
        <div class="c4-align">
           <div>
                <h1>IMPRESIONA AL MUNDO <span style="color: #F26800; font-weight: bold;">CON NOSOTROS</span></h1>
                <h3>Si tienes algo en mente, es hora de comenzar</h3>
           </div>
        </div>
    </div>

    <div class="container-five">
        <div class="container">
            <h2 class="title-two">Nuestro Trato Con Nuestros Clientes</h2>
            <div style="width: 100px; border-bottom: 3px solid #F26800; margin: auto;"></div>
        </div>
        <div style="margin-top: 30px;">
            <div class="c5-flex c5-ld">
                <img class="treat-icons" src="../img/respect.png">
                <h4 class="treat-subtitles">Respeto</h4>
                <p class="p-border">El respeto a la persona y al negocio es uno de los valores fundamentales para nosotros. Por eso, siempre vamos a ofrecer un trato de excelente calidad a nuestros clientes, para que tengan ganas de volver a nosotros, y por supuesto, por nuestro trabajo de calidad.</p>
                <img class="treat-icons" src="../img/commitment.png">
                <h4 class="treat-subtitles">Compromiso</h4>
                <p>Estamos 100% comprometidos a realizar trabajos excepcionales para crear una gran imagen a nuestros clientes, con sitios totalmente personalizados y adaptados según se solicite. Parte de nuestro compromiso es darle estabilidad y seguridad al cliente.</p>
            </div>
            <div class="c5-flex">
                <img class="treat-icons" src="../img/support.png">
                <h4 class="treat-subtitles">Seguimiento</h4>
                <p class="p-border">Siempre al finalizar el trabajo solicitado por el cliente, se le va a dar el debido seguimiento, para asegurar la calidad y durabilidad del servicio. También, siempre vamos a estar disponibles para que nos contacten cuando nos necesiten, ofreciendo nuestra mejor versión.</p>
                <img class="treat-icons" src="../img/kindness.png">
                <h4 class="treat-subtitles">Amabilidad</h4>
                <p>Un trato amable es lo que van a recibir en Art Development, porque en el trabajo somos todos un mismo equipo.</p>
            </div>
        </div>
    </div>

</template>

<style scoped>

.bg-one{
    background-image: url(../img/bg-one.jpg);
    background-repeat: no-repeat;
    background-size: cover;
}

/* ----------------------------CONTAINER ONE-------------------------------- */
.container-one{
    color: #ffffff;
    padding-top: 160px;
    padding-bottom: 100px;
    height: 100%;
    text-align: center;
}

.c1-title{
    font-weight: bold;
}

.c1-title, .c1-p1{
    text-align: justify;
}

.c1-p1{
    margin-bottom: 40px;
}

.c1-p2, .c1-p3{
    text-align: center;
}

.orange-btn{
    color: #ffffff;
    background-color: #F26800 ;
    border: none;
    padding: 10px 20px 10px 20px;
    margin-top: 10px;
    font-weight: bold;
}
.orange-btn:hover{
    background-color: #ff7b17 ;
    transform: scale(1.01);
}
/* 
-------------------------------CONTAINER TWO---------------------------- */
.container-two p{
    color: rgb(68, 68, 68);
}
.c2-title{
    padding: 30px 0 0px 0; 
    font-weight: bold;
}
.c2-flex{
    display: flex;
}
.title-two{
    padding-top: 50px;
    font-weight: bold;
}
.c2-project-content{
    text-align: justify;
    padding-right: 20px;
    width: 100%;
}
.c2-project-content-img{
    width: 100%;
    text-align: center;
}
.c2-img-creativity{
    width: 100%;
}
/* 
-------------------------------CONTAINER THREE---------------------------- */
.container-three h4{
    margin-top: 40px; 
    font-weight: bold;
}

.container-three p{
    margin-top: 10px;
}
.container-three{
    text-align: center; 
    background-color: #29291e; 
    padding: 50px 0px 100px 0px; 
    margin-top: 10px;
    color: white;
}
.btn-services{
    color: white;
    background-color: transparent;
    padding: 10px 20px 10px 20px;
    margin-top: 10px;
    font-weight: bold;
    border: 1px solid white;
}
.btn-services:hover{
    background-color: white;
    border: 1px solid black;
    color: black;
    transform: scale(1.01);
}
/* 
-------------------------------CONTAINER FOUR---------------------------- */
.container-four{
    text-align: center;
    color: white;
    height: 400px;
    background-image: url(../img/worldImg.jpg);
    background-attachment: fixed;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
}

.c4-align{
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.404);
}

/* ------------------------------CONTAINER FIVE----------------------- */
.container-five{
    text-align: center;
    width: 100%;
    margin-bottom: 30px;
}
.container-five p{
    color: rgb(68, 68, 68);
}
.treat-icons{
    width: 45px;
    margin-top: 50px;
}
.treat-subtitles{
    font-weight: bold;
}
.c5-flex{
    display: inline-block;
    width: 40%;
    padding: 20px;
    text-align: justify;
    box-shadow: 0px 0px 14px -11px rgba(0,0,0,1);
-webkit-box-shadow: 0px 0px 14px -11px rgba(0,0,0,1);
-moz-box-shadow: 0px 0px 14px -11px rgba(0,0,0,1);
}
.c5-ld{
    border-right: 1px solid rgb(245, 245, 245);
}
.p-border{
    border-bottom: 1px solid rgb(245, 245, 245);
}

@media screen and (max-width: 1000px){

    .orange-btn{
        color: #ffffff;
        background-color: #F26800 ;
        border: none;
        padding: 10px 20px 10px 20px;
        margin-top: 10px;
        margin-bottom: 20px;
        font-weight: bold;
    }

    /* 
    -------------------------------CONTAINER TWO---------------------------- */
    .c2-flex{
    display: block;
    }
    .c2-project-content{
        text-align: center;
        padding: 0;
        width: 100%;
    }
    .c2-project-content-img{
        width: 100%;
        text-align: center;
    }
    .c2-img-creativity{
        width: 100%;
    }
    /* 
    -------------------------------CONTAINER THREE---------------------------- */
    .container-three h4{
        margin-top: 40px; 
        font-weight: bold;
    }

    .container-three p{
        margin-top: 10px;
    }
    .container-three{
        text-align: center; 
        background-color: #14140F; 
        padding: 50px 0px 100px 0px; 
        margin-top: 10px;
        color: white;
    }
    .btn-services{
        color: white;
        background-color: transparent;
        padding: 10px 20px 10px 20px;
        margin-top: 10px;
        font-weight: bold;
        border: 1px solid white;
    }
    /* 
    -------------------------------CONTAINER FOUR---------------------------- */
    .container-four{
        text-align: center;
        color: white;
        height: 400px;
        background-image: url(../img/worldImg.jpg);
        background-attachment: initial;
        background-repeat: no-repeat;
        background-size: cover;
    }

    /* ------------------------------CONTAINER FIVE----------------------- */
    .c5-flex{
        display: inline-block;
        width: 90%;
        border: none;
        padding: 20px;
        text-align: justify;
        box-shadow: 0px 0px 14px -11px rgba(0,0,0,1);
        -webkit-box-shadow: 0px 0px 14px -11px rgba(0,0,0,1);
        -moz-box-shadow: 0px 0px 14px -11px rgba(0,0,0,1);
    }
    .p-border{
    border: none;
    }
}

</style>

