<script>
import {RouterView } from 'vue-router'
import navigation from '@/components/nav.vue'
import sfooter from '@/components/footer.vue'

export default {
  components: {
    navigation,
    sfooter,
  }
}
</script>

<template>
  
  <navigation></navigation>
  <RouterView />
  <sfooter></sfooter>
</template>

<style scoped>

</style>
