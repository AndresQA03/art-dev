<script allowjs="true">
import Home from '@/components/Home.vue'
import Email from '@/components/ContactForm.vue'
import CardsCarousel from '@/components/CardsCarousel.vue'

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
        Home,
        Email,
        CardsCarousel
    },
    mixins: [resetScrollMixin],
}
</script>
<template>
<Home></Home>
<CardsCarousel></CardsCarousel>
<Email></Email>
</template>