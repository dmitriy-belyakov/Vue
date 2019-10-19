<template>
  <div id="app">
    <Form/>
  </div>
</template>

<script>
import Form from './components/Form.vue'

export default {
  name: 'app', 
  components: {
    Form,
  } 
}
</script>

<style>
#app{
  margin-top: 100px;
  margin-left: 200px;
  border: 4px double black;
  background: #18101A;  
  height: 350px;
  width: 600px;  
}
</style>
