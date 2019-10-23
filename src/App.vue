<template>
  <div id="app">
    <Header/>
    <Menu/>
    <Table/>
    <edtinp :title = "first_name" v-model="first_name" @save = "save"/>
  </div>
</template>

<script>
import Menu from '@/components/Menu.vue'
import Header from '@/components/Header.vue'
import Table from '@/components/Table.vue'
import edtinp from '@/components/edt_inp.vue'

export default {
  name: 'app',
  components: {
    Menu, Header, Table, edtinp
  },
  data () {
    return {
      first_name: 'Ann'
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
