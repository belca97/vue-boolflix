<template>
        <main>

        </main>
</template>

<script>
export default {
    name: 'MyMain',
    props: {
        'films': Array
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