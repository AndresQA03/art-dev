<script allowjs="true">
import Services from '@/components/Services.vue';
import CardsCarousel from '@/components/CardsCarousel.vue';

const resetScrollMixin = {
  watch: {
    $route () {
        this.$nextTick(() => {
        window.scrollTo(0, 0)
    })
    }
  }
}

export default{
    components: {
        Services,
        CardsCarousel
    },
    mixins: [resetScrollMixin],
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