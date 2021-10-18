<template>
  <div>
    <input :value="value" @input="onInput" />
  </div>
</template>
<script>
export default {
  props:["value"],
  methods:{
    onInput(e){
      const data =e.target.value
      this.$emit("input",data)
    }
  }
}
</script>
<style scoped>

</style>