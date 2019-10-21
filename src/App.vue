<template>
  <div id="app">
    <Header/>
    <Menu/>
  </div>
</template>

<script>
import Menu from '@/components/Menu.vue'
import Header from '@/components/Header.vue'

export default {
  name: 'app',
  components: {
    Menu, Header
  }
}
</script>

<style>
  body, html{
    margin: 0;
    padding: 0;
  }
  #app{
    height: auto;
  }
</style>
