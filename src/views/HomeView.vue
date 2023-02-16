<script>
import Home from '@/components/Home.vue'
import Email from '@/components/ContactForm.vue'
import CardsCarousel from '@/components/CardsCarousel.vue'

export default{
    components: {
        Home,
        Email,
        CardsCarousel
    },

}
</script>
<template>
<Home></Home>
<CardsCarousel></CardsCarousel>
<Email></Email>
</template>