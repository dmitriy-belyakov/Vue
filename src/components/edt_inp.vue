<template>
  <div id="edt_inp">
    <span v-if="!changing">
        {{ title }}
    </span>
    <input
        v-if="changing"
        :placeholder="title"
    />
    <img width = 20 height = 20 src = "../../icons/edit.svg" v-if="!changing" @click = "changing = !changing">
    <img width = 20 height = 20 src = "../../icons/accept.svg" v-if="changing" @click = "changing = !changing">
    <!-- <img width = 20 height = 20 src = "../../icons/clear.svg" v-if="changing" @click = "cancel"> -->
  </div>
</template>

<script>
export default {
  name: 'edt_inp',
  props: ['title'],
  data () {
    return {
      changing: false
    }
  }
}
</script>

<style scoped>
  #check{
    float: bottom;
    margin: 0 auto;
    width: 30vh;
  }
  .el-input{
    width: 20vh;
  }
  img{
    margin-left: 2%;
  }
</style>
