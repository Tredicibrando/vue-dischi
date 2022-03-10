<template>
    <section class="content">
        <div class="container">
            <MyCard />
            <MyCard />
            <MyCard />
            <MyCard />
            <MyCard />
            <MyCard />
            <MyCard />
            <MyCard />
            <MyCard />
            <MyCard />

        </div>
    </section>
</template>

<script>
import MyCard from '@/components/MyCard'
    export default {
        name:'MyContent',

        components: {
            MyCard,
        },

        data(){
            
        }


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