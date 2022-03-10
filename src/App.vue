<template>
  <div id="app">
    <MyMain />
  </div>
</template>

<script>
import MyMain from '@/components/MyMain'


export default {
  name: 'App',
  components: {
          MyMain,
  }
}
</script>

<style lang="scss">

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

}
</style>
