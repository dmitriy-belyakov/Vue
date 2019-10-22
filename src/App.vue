<template>
  <div id="app">
    <Header/>
    <Menu/>
    <Table/>
  </div>
</template>

<script>
import Menu from '@/components/Menu.vue'
import Header from '@/components/Header.vue'
import Table from '@/components/Table.vue'

export default {
  name: 'app',
  components: {
    Menu, Header, Table
  }
}
</script>

<style>
  body, html{
    margin: 0;
    padding: 0;
    background: white;
  }
  #app{
    height: 100%;
    width: 100%;
  }
</style>
