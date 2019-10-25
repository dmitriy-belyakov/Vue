<template>
  <div class="editinp">
    <span v-if="!changing">
        {{ value }}
    </span>
    <input
        v-if="changing"
        :placeholder="value"
        v-model="string"
    />
    <img src="../../icons/edit.svg" v-if="!changing" @click="changing=true">
    <img src="../../icons/accept.svg" v-if="changing" @click="save">
    <img src="../../icons/clear.svg" v-if="changing" @click="cancel">
  </div>
</template>

<script>
export default {
  name: 'editinp',
  props: ['value'],
  data () {
    return {
      changing: false,
      string: this.value
    }
  },
  methods: {
    save () {
      this.changing = false
      this.$emit('input', this.string)
    },
    cancel () {
      this.string = this.value
      this.changing = false
    }
  }
}
</script>

<style scoped>
  .editinp{
    float: left;
    min-width: 140px;
    margin-left: 500px;
  }
  img{
    margin-left: 20px;
    margin-bottom: -5px;
    width: 20px;
    height: 20px;
  }
</style>
