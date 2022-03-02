<template>

        <header>
            <h1>BOOLFIX</h1>
            <form>
                <input type="text" v-model="searchText">
                <button type='submit' @click.prevent="search">Ricerca</button>
            </form>
        </header>
</template>

<script>
export default {
    name:'MyHeader',
    data(){
        return{
            searchText: '',
        }
    },
    methods:{
        search(){
            this.$emit('search', this.searchText)
        }
    }
}
</script>

<style scoped lang='scss'>

    header{
        background-color: black;
        color: red;
        height: 10vh;
        display: flex;
        align-items: center;

            h1{
                float: left;
                width: 50%;
                text-align: left;
                padding: 0px 20px;
            }
            form{
                float: right;
                width: 50%;
                text-align: right;
                padding: 0px 20px;

                button{
                    background-color: orange;
                    padding: 3px 3px;
                    margin-left: 5px;
                    border-radius: 5px;
                }
            }
    }
    header::after{
        display: table;
        clear: both;
        content: '';
    }
    

</style>