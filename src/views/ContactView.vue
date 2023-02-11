<script allowjs="true">
import ContactForm from '@/components/ContactForm.vue';

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
        ContactForm,
    },
    mixins: [resetScrollMixin],
}
</script>
<template>
    <div class="space"></div>
    <ContactForm></ContactForm>
    <div class="space2"></div>
</template>

<style scoped>
.space{
    height: 100px;
    background-color: #29291e;
}
/* .space2{
    height: 100vh;
    background-color: #14140F;
} */
</style>