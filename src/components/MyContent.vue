<template>
    <section class="content">
        <div class="container">
            <MyCard v-for="(element,i) in discs" :key="i" :element="element" />

        </div>
    </section>
</template>

<script>
import MyCard from '@/components/MyCard'
import axios from 'axios'

    export default {
        name:'MyContent',


        components: {
            MyCard,
        },

        data(){
            return{
                discs: [],
            }
        },

        methods: {
            getDisc: function(){
                    axios.get('https://flynn.boolean.careers/exercises/api/array/music')
                    .then( res =>{
                        // console.log(res.data.response)
                        this.discs = res.data.response;
                        console.log(this.discs)
                    })
                }
        },

        created(){
            this.getDisc()
        },

    }
</script>

<style lang="scss" scoped>
    .content{
        height: calc(100vh - 70px );
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 40px 0;


        .container{
            width: 1170px;
            margin: 0 auto;
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
            justify-content: center;

        }
    }
</style>