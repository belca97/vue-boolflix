<template>
        <main>
            <FilmsList :films="films"/>
        </main>
</template>

<script>

    import FilmsList from './FilmsList.vue'

export default {

    name: 'MyMain',
    props: {
        'films': Array
    },
    components:{
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