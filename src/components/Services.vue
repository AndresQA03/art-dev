<script>

</script>
<template>
    <div class="container-one-s">
        <div class="bg-color">
            <div class="cont-content container">
                <h1>{{ $t("services.container-one.header") }}</h1>
                <img class="arrow" src="../img/downArrow.png">
            </div>
        </div>
    </div>
    <div class="container-two-s">
        <h2 >{{ $t("services.container-two.header") }}</h2>
        <div style="width: 100px; border-bottom: 3px solid #F26800; margin: auto;"></div>
        <h4 class="cts-subtitle-two">{{ $t("services.container-two.st1") }}</h4>
        <div>
            <div class="c5-flex c5-ld">
                <h4>{{ $t("services.container-two.st2") }} <img class="icons-c2" src="../img/projectsIcon.png"></h4>
                <p>{{ $t("services.container-two.t1") }}</p>
                <h4> {{ $t("services.container-two.st3") }}<img class="icons-c2" src="../img/timerIcon.png"></h4>
                <p>{{ $t("services.container-two.t2") }}</p>
                <h4> {{ $t("services.container-two.st4") }}<img class="icons-c2" src="../img/pricesIcon.png"></h4>
                <p>{{ $t("services.container-two.t3") }} <RouterLink to="contact">{{ $t("services.container-two.t4") }}</RouterLink> {{ $t("services.container-two.t5") }}</p>
            </div>
            <div class="c5-flex">
                <h4>{{ $t("services.container-two.st5") }}<img class="icons-c2" src="../img/contractIcon.png"></h4>
                <p>{{ $t("services.container-two.t6") }}</p>
                <h4>{{ $t("services.container-two.st6") }} <img class="icons-c2" src="../img/guaranteeIcon.png"></h4>
                <p>{{ $t("services.container-two.t7") }}</p>
                <h4> {{ $t("services.container-two.st7") }}<img class="icons-c2" src="../img/support2Icon.png"></h4>
                <p>{{ $t("services.container-two.t8") }}</p>
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