<template>
  <div class="hello">
    <div id = "header">
      <a @click="home_click"> Home </a>
      <a @click="about_click"> About </a>
      <a @click="FAQ_click"> FAQ </a>
    </div>
    <component :is="Current"></component>
  </div>
</template>

<script>
import Home from './Home.vue'
import About from './About.vue'
import FAQ from './FAQ.vue'
export default {
  name: 'hello', 
  data (){ 
    return{
      Current: Home
    }
  },
  components: {
    Home, About, FAQ
  }, 
  methods: {
      home_click() {
        this.Current = Home
      },
      about_click() {
        this.Current = About
      },
      FAQ_click() {
        this.Current = FAQ
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

#header{
  display: flex;
  justify-content: space-around;
  background: black;
  padding: 0;
  margin: 0;
}

#content{
  display: flex;
  justify-content: space-around;
  padding: 0;
  margin: 0;
}

a{
  color: white;
	text-shadow: 0 -1px 4px #FFF, 0 -2px 10px #ff0, 0 -10px 20px #ff8000, 0 -18px 40px #F00;
	font-size: 15pt;
	text-decoration:none;
}

a:hover{
  border-bottom: 2px solid orange;
	cursor: pointer;
}

</style>
