<template>
    <main>
        <MyHeader @input="setFilter" />
        <MyContent :filter="selectedFiltrata"/>
    </main>
</template>

<script>
import MyHeader from '@/components/MyHeader'
import MyContent from '@/components/MyContent'

    export default {
        name:'MyMain',

        components:{
                MyHeader,
                MyContent,
        },

        data(){
            return{
                selectedFiltrata: '',
            }
            
        },

        methods:{
            setFilter: function(selected){
                
                this.selectedFiltrata = selected;
                console.log(this.selectedFiltrata)
            }
        },
    }
</script>

<style lang="scss" scoped>

    $bg: #1E2D3B; 
    main{
        width: 100%;
        height: 100vh;
        background-color: $bg;
    }
</style>