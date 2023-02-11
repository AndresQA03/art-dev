<script allowjs="true">
import LanguagesSwitcher from '@/components/LanguagesSwitcher.vue';
import Tr from "@/i18n/translation"

export default{
    components: {
        LanguagesSwitcher,
    },
    setup(){
        return{Tr};
    },
    data () {
        return {
        view: {
            topOfPage: true
        }
        }
    },
    beforeMount() {
        window.addEventListener('scroll', this.handleScroll)

    },

    methods: {
        handleScroll(){
            if(window.pageYOffset>0){
                if(this.view.topOfPage) this.view.topOfPage = false
            } else {
                if(!this.view.topOfPage) this.view.topOfPage = true
            }
        }
    }
}
</script>
<template>
    <nav class="navbar navbar-expand-lg navbar-dark" :class="{ 'onScroll': !view.topOfPage}">
        <div class="container-fluid">
        <a class="navbar-brand" href="#" style="font-weight: bold;"><img src="../assets/fondoN.png" class="logo">ART<span style="color: #F26800;">DEVELOPMENT</span></a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse justify-content-end" id="navbarSupportedContent">
            <ul class="navbar-nav">
            <li class="nav-item">
                <RouterLink class="nav-link" active-class="active-link" exact-active-class="exact-active-link" aria-current="page" :to="Tr.i18nRoute({name: 'home'})">{{ $t("nav.home") }}</RouterLink>
            </li>
            <li class="nav-item">
                <RouterLink class="nav-link" active-class="active-link" exact-active-class="exact-active-link" aria-current="page" :to="Tr.i18nRoute({name: 'services'})">{{ $t("nav.services") }}</RouterLink>
            </li>
            <li class="nav-item">
                <RouterLink class="nav-link" active-class="active-link" exact-active-class="exact-active-link" aria-current="page" :to="Tr.i18nRoute({name: 'contact'})">{{ $t("nav.contact") }}</RouterLink>
            </li>
            </ul>
            <LanguagesSwitcher></LanguagesSwitcher>
        </div>
        </div>
    </nav>
</template>

<style scoped lang="scss">
.active {
    
}

.exact-active-link {
    font-weight: bold;
    background-color: black;
    color: #F26800;
}

nav {
    position: fixed;
    z-index: 5;
    width: 100%;
    background-color: transparent;
    transition: all .2s ease-in-out;
    &.onScroll {
      background-color: #14140F;
        .exact-active-link {
            font-weight: bold;
            background-color: #F26800;
            color: black;
        }
    }
  }
.navbar-collapse{
    text-align: center;
}
a{
  color: #ffffff;
}
.logo{
  width: 100px;
  margin-right: 10px;
  margin-left: 10px;
}

@media screen and (max-width: 1000px){
    nav{
        position: initial;
        width: 100%;
        background-color: #14140F;
    }
    .exact-active-link {
            font-weight: bold;
            background-color: #F26800;
            color: black;
        }
}
@media screen and (max-width: 400px){
    .logo{
        width: 80px;
        margin-right: 10px;
        margin-left: 10px;
    }
}
</style>