<template>
  <div>
    {{user.userName}}
    <hr>
    {{user.userPassword}}
    <myInput :value="user.userName" @input="user.userName=$event" />
    <myInput v-model="user.userPassword" />
  </div>

</template>
<script>
import myInput from "./components/model"

export default {
  components: {myInput},
  data(){
    return {
      user:{
        userName:"李白",
        userPassword:"123"
      }
    }
  }
}
</script>
<style scoped>

</style>