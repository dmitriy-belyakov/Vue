<template>
  <div id="app">
    <Menu/>
  </div>
</template>

<script>
import Menu from '@/components/Menu.vue'

export default {
  name: 'home',
  components: {
    Menu
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
