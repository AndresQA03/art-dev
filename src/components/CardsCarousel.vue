<script>
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'

export default {
  name: 'MyComponent',
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation,
  },
  computed: {
    translatedSlides() {
      return new Array(
        { id: '1', icon: 'https://res.cloudinary.com/dvbrbluvn/image/upload/v1675369251/webIcon_prtcng.png', title: 'DESARROLLO WEB', content: 'Damos vida a tus ideas utilizando frameworks de JavaScript para la elaboración de el sitio web'},
        { id: '2', icon: 'https://res.cloudinary.com/dvbrbluvn/image/upload/v1675369210/support2Icon_cv4ghc.png', title: 'SOPORTE', content: 'Soporte 100% disponible, no solo de programas desarrollados por nosotros, si tienes un sitio y no tienes con quien darle mantenimiento, también puedes contactarnos' },
        { id: '3', icon: 'https://res.cloudinary.com/dvbrbluvn/image/upload/v1675369219/hostingIcon_kdnaox.png', title: 'HOSTING', content: 'Nosotros nos encargamos de subir tu sitio a los servidores, de tal manera que no te tengas que preocupar de eso. Siempre arriba en la web!'},
        { id: '4', icon: 'https://res.cloudinary.com/dvbrbluvn/image/upload/v1675369216/othersIcon_s6qcyg.png', title: 'OTROS', content: 'Desarrollo de aplicaciones web, bases de datos, programas de consola, entre otros.. Solo contactanos y te ayudaremos'}
        );
    },
  },
  data() {
    return {
      breakpoints: {
        // 700px and up
        700: {
          itemsToShow: 2,
          snapAlign: 'center',
        },
        // 1024 and up
        1024: {
          itemsToShow: 2,
          snapAlign: 'center',
        },
      },
    }
  },
}
</script>

<template>
    <div class="wrapper" >
        <h1>EN QUÉ PODEMOS AYUDARTE?</h1>
        <div style="width: 200px; border-bottom: 3px solid #F26800; margin: auto;"></div>
        <Carousel :wrap-around="true" :breakpoints="breakpoints" :autoplay="8000" >
            <Slide v-for="slide in translatedSlides" :key="slide.id">
            <div class="carousel__item">
                <div style="background-color: #29291e; padding: 20px 10px 10px 10px; margin-bottom: 10px;">
                    <img :src="slide.icon">
                    <h3>{{ slide.title }}</h3>
                </div>
                <p>{{ slide.content }}</p>
            </div>
            </Slide>

            <template #addons>
            <Navigation />
            <Pagination />
            </template>
        </Carousel>
    </div>
</template>

<style scoped>
img{
    width: 40px;
    margin-bottom: 10px;
}
.wrapper{
    padding: 100px 0 80px 0;
    background-image: url(../img/skills.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    text-align: center;
}
.wrapper h1{
    color: white;
}
.carousel__item {
  min-height: 350px;
  width: 90%;
  background-color: rgb(255, 255, 255);
  color: black;
  font-size: 20px;
  border-radius: 8px;
  justify-content: center;
  align-items: center;
   margin-top: 20px;
    padding: 30px;
    margin-bottom: 30px;
}

.carousel__item h3{
    color: white;
}

.carousel__prev,
.carousel__next {
  box-sizing: content-box;
  border: 5px solid white;
}

</style>