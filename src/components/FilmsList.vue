
<template>
<!-- componente che serve per contenere le card -->
  <ul>
      <FilmCard v-for='(film, index) in films' :key="index" :film='film'/>
  </ul>
</template>

<script>

import FilmCard from './partials/FilmCard.vue'

export default {
    name: 'FilmsList',
        props: {
        'films': Array
    },
    components: {
        FilmCard
    }
}
</script>

<style scoped lang='scss'>

</style>