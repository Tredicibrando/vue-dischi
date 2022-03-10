<template>
    <header class="header_wrapper">
        <figure class="logo__wrapper">
            <img class="logo" src="../assets/img/spotify-2.svg" alt="">
        </figure>
    </header>
</template>

<script>
    export default {
            name:'MyHeader',
    }
</script>

<style lang="scss" scoped>


    .header_wrapper{
        width: 100%;
        height: 70px;
        background-color:#2E3A46;
        display: flex;
        align-items: center;

        .logo__wrapper{
            width: max-content;
            padding: 5px 10px;

            .logo{
                width: 55px;
                display: block;

            }
        }

    }
</style>