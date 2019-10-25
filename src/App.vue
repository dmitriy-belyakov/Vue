<template>
  <div id="app">
    <Header/>
    <Menu/>
    <Table/>
    <editinp v-model="val"/>
  </div>
</template>

<script>
import Menu from '@/components/Menu.vue'
import Header from '@/components/Header.vue'
import Table from '@/components/Table.vue'
import editinp from '@/components/editinp.vue'

export default {
  name: 'app',
  components: {
    Menu, Header, Table, editinp
  },
  data () {
    return {
      val: 'Ann'
    }
  },
  methods: {
    save (title) {
      this.first_name = title
    }
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
