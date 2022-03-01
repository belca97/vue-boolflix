<template>
        <main>
            <FilmsList />
        </main>
</template>

<script>

    import FilmsList from  './FilmsList.vue'

export default {

    name: 'MyMain',
    props: {
        'films': Array
    },
    componets: {
      FilmsList
    }
}
</script>

<style scoped lang='scss'>

@import './src/assets/style/variabili.scss';

main{
    height: 90vh;
    background-color: $colorMain;
}
</style>