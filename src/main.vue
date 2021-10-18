<template>
  <div>
    {{ user.userName }}
    <hr>
    {{ user.userPassword }}
    <myInput :value="user.userName" @input="user.userName=$event"/>
    <myInput v-model="user.userPassword"/>
    <hr>
    <hr>
    <div>{{ user.userName }}</div>
    <input2 :value="user.userName" @input2= "changeName" />
    <input2 :value="user.userPassword" @input2= "changPassword" />

  </div>

</template>
<script>
import myInput from "./components/model.vue"
import input2 from "./components/myInput.vue"

export default {
  components: {
    myInput: myInput,
    input2: input2
  },
  data() {
    return {
      user: {
        userName: "李白",
        userPassword: "123"
      }
    }
  },
  methods:{
    changeName(event){
      this.user.userName=event
    },
    changPassword(event){
      this.user.userPassword=event
    }
  }
}
</script>
<style scoped>

</style>