<script>
  import { useI18n } from 'vue-i18n'
  import { useRouter } from "vue-router"
  import Tr from "@/i18n/translation"
  export default {
    setup() {
      const { t, locale } = useI18n()
      const supportedLocales = Tr.supportedLocales
      const router = useRouter()
      const switchLanguage = async (event) => {
        const newLocale = event.target.value
        await Tr.switchLanguage(newLocale)
        try {
          await router.replace({ params: { locale: newLocale } })
        } catch(e) {
          console.log(e)
          router.push("/")
        }
      }
      return { t, locale, supportedLocales, switchLanguage }
    }
  }
</script>

<template>
   <label>
    <select @change="switchLanguage">
    <option
      v-for="sLocale in supportedLocales"
      :key="`locale-${sLocale}`"
      :value="sLocale"
      :selected="locale === sLocale"
      style="color: black;"
    >
      {{ t(`locale.${sLocale}`) }}
    </option>
  </select>
   </label>
</template>

<style scoped lang="scss" >
label {
  position: relative;
  display: inline-block;
  &:after {
    content: '▼';
    position: absolute;
    width: 36px;
    color: #ffffff;
    font-weight: bold;
    font-size: 16px;
    right: 2px;
    bottom: 8px;
    -webkit-border-radius: 3px;
    -moz-border-radius: 3px;
    border-radius: 3px;
    pointer-events: none;
    z-index: 2;
  }
  &:before {
    content: '';
    right: 2px;
    top: 2px;
    width: 37px;
    height: 34px;
    background: #14140F;
    position: absolute;
    pointer-events: none;
    display: block;
    z-index: 1;
    -webkit-border-radius: 3px;
    -moz-border-radius: 3px;
    border-radius: 3px;
  }
  select {
    position: relative;
    width: 150px;
    -webkit-appearance: none;
    -moz-appearance: none;
    appearance: none;
    background: none;
    color: #ffffff;
    border: 1px solid #ffffff;
    outline: none;
    padding-left: 7px;
    margin: 0 0 0 5px;
    -webkit-border-radius: 3px;
    -moz-border-radius: 3px;
    border-radius: 3px;
    cursor: pointer;
    height: 38px;
  }
}
</style>
