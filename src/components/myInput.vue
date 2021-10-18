<template>
  <div>
    <input type="text" :value="value" @input="submit">
  </div>
</template>
<script>
export default {
  props:["value"],
  methods:{
    submit(e){
      const event=e.target.value
      this.$emit("input2",event)
    }
  }
}
</script>