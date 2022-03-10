<template>
    <div class="card">
        <figure class="disc_wrapper">
            <img class="disc" src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
        </figure>

        <div class="card_text_wrapper">
            <h4 class="title">Ten summoners names dio</h4>
            <p class="author">Max Felicitas</p>
            <p class="year">1988</p>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'MyCard',
        
        props:{
            
        }


    }
</script>

<style lang="scss" scoped>
.card{
    width: calc((100% - 50px) / 5);
    padding: 10px;
    height: 360px;
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: #2E3A46;

    .disc_wrapper{
        width: 100%;
        height: 200px;
        margin-bottom: 25px;

        img{
            width: 100%;
            object-position: center;
            object-fit: cover;
        }


    }

    .card_text_wrapper{
        text-align: center;
        width: 70%;

        .title{
            margin-bottom: 20px;
            font-weight: 700;
            color: white;
            text-transform: uppercase;
        }

        .author{
            font-size: 16px;
            color: rgba($color: #ddd, $alpha: 0.7);
            margin-bottom: 5px;
        }

        .year{
            font-size: 14px;
            color: #ddd;
        }




    }
}
</style>