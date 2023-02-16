<script>
import Services from '@/components/Services.vue';
import CardsCarousel from '@/components/CardsCarousel.vue';

export default{
    components: {
        Services,
        CardsCarousel
    },

}

</script>

<template>
    <Services></Services>
    <CardsCarousel class="cards-services-view"></CardsCarousel>
</template>

<style scoped>
.cards-services-view{
    margin-top: 50px;
}
</style>