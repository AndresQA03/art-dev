<script allowjs="true">
import Tr from "@/i18n/translation"

export default{
    setup(){
        return{Tr};
    },
}
</script>
<template>

    <div class="bg-one">
        <div style="background-color: rgba(0, 0, 0, 0.616);">
            <div class="container container-one">
                <h1 class="c1-title">{{ $t("home.container-one.header") }}</h1>
                <h2 class="c1-p1">{{ $t("home.container-one.t1") }}</h2>
                <h2 class="c1-p2">{{ $t("home.container-one.t2") }}<span style="font-weight: bold"> Art Development</span></h2>
                <h2 class="c1-p3">{{ $t("home.container-one.t3") }}</h2>
                <a href="https://msng.link/o/?artdevelopment__=ig" target="_blank"><button class="orange-btn" role="link">{{ $t("home.container-one.t4") }}</button></a>
            </div>
        </div>
    </div>

    <div class="container container-two">
        <h2 class="c2-title">{{ $t("home.container-two.header") }}</h2>
        <div style="width: 100px; border-bottom: 3px solid #F26800; margin-bottom: 15px;"></div>
        <div class="c2-flex">
            <div class="c2-project-content">
                <h4>{{ $t("home.container-two.st1") }}</h4>
                <p>{{ $t("home.container-two.t1") }}</p>
                <p>{{ $t("home.container-two.t2") }}</p>
                <RouterLink class="nav-link" active-class="active-link" exact-active-class="exact-active-link" aria-current="page" :to="Tr.i18nRoute({name: 'contact'})"><button class="orange-btn">{{ $t("home.container-two.btn1-t") }}</button></RouterLink>
            </div>
            <div class="c2-project-content-img">
                <img class="c2-img-creativity" src="../img/creativity.jpg">
            </div>
        </div>
    </div>

    <div class="container-three" style="">
        <div class="container">
            <h4>{{ $t("home.container-three.header") }}</h4>
            <div style="width: 200px; border-bottom: 3px solid #F26800; margin: auto;"></div>
            <p>{{ $t("home.container-three.t1") }}</p>
            <RouterLink class="nav-link" active-class="active-link" exact-active-class="exact-active-link" aria-current="page" :to="Tr.i18nRoute({name: 'services'})"><button class=" btn-services">{{ $t("home.container-three.btn1-t") }}</button></RouterLink>
        </div>
    </div>

    <div class="container-four">
        <div class="c4-align">
           <div>
                <h1>{{ $t("home.container-four.header") }} <span style="color: #F26800; font-weight: bold;">{{ $t("home.container-four.header2") }}</span></h1>
                <h3>{{ $t("home.container-four.t1") }}</h3>
           </div>
        </div>
    </div>

    <div class="container-five">
        <div class="container">
            <h2 class="title-two">{{ $t("home.container-five.header") }}</h2>
            <div style="width: 100px; border-bottom: 3px solid #F26800; margin: auto;"></div>
        </div>
        <div style="margin-top: 30px;">
            <div class="c5-flex c5-ld">
                <img class="treat-icons" src="../img/respect.png">
                <h4 class="treat-subtitles">{{ $t("home.container-five.st1") }}</h4>
                <p class="p-border">{{ $t("home.container-five.t1") }}</p>
                <img class="treat-icons" src="../img/commitment.png">
                <h4 class="treat-subtitles">{{ $t("home.container-five.st2") }}</h4>
                <p>{{ $t("home.container-five.t2") }}</p>
            </div>
            <div class="c5-flex">
                <img class="treat-icons" src="../img/support.png">
                <h4 class="treat-subtitles">{{ $t("home.container-five.st3") }}</h4>
                <p class="p-border">{{ $t("home.container-five.t3") }}</p>
                <img class="treat-icons" src="../img/kindness.png">
                <h4 class="treat-subtitles">{{ $t("home.container-five.st4") }}</h4>
                <p>{{ $t("home.container-five.t4") }}</p>
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

