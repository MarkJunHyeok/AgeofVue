<script>
import axios from "axios";

export default {
  data() {
    return {
      username : '',
      password : ''
    }
  },
  methods: {
    submitForm() {
      var url = 'https://jsonplaceholder.typicode.com/users'
      var data = {
        username: this.username,
        password: this.password
      }

      axios.post(url, data)
          .then(function (response) {
            console.log(response)
          }).catch(function (error) {
        console.log(error)
      })
    }
  }
}
</script>

<template>
  <form v-on:submit.prevent="submitForm">
    <div>
      <lable for="username">id:</lable>
      <input id="username" type="text" v-model="username" />
    </div>
    <div>
      <lable for="password">password:</lable>
      <input id="password" type="password" v-model="password" />
    </div>
    <button type="submit">login</button>
  </form>
</template>

<style scoped>

</style>