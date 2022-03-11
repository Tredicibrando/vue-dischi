<template>
    <nav class="header_wrapper">
        <figure class="logo__wrapper">
            <img class="logo" src="../assets/img/spotify-2.svg" alt="">
        </figure>

        <select v-model="selected" class="select" name="options" @change="FiltraSelect" >
            <option v-for="(opzione,i) in valoriArray" :key="i" v-bind:selected="opzione.valore"  >{{opzione.testo}}</option>
        </select>
    </nav>
</template>

<script>
    export default {
            name:'MyHeader',
            data(){
                return{
                    selected: '',
                    valoriArray:[
                        {
                            valore: '1',
                            testo: 'Pop',
                        },
                         {
                            valore: '2',
                            testo: 'Metal',
                        },
                         {
                            valore: '3',
                            testo: 'Rock',
                        },
                         {
                            valore: '4',
                            testo: 'Jazz',
                        },
                    ],
                }
            },
            methods:{
                FiltraSelect: function(){
                    console.log(this.selected)
                    this.$emit('input',this.selected) 
                },
            },
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


        .select{
            font-size: 18px;
            width: 250px;
            background-color: #2E3A46;
            color: white;
            border: 1px solid white;
            border-radius: 8px;
            margin: 0 auto;


        }
    }
</style>