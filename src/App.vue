<template>
  <input v-model="user.name">
  <input type="password" v-model="user.pass">

  <button @click="authorize(user.name, user.pass)">Log in</button>

  <pre>{{ user | json }}</pre>
</template>

<script>
export default {
  data () {
    return {
      user: {
        name: "",
        pass: ""
      }
    }
  },
  methods: {
    authorize (username, password) {
      console.log(password)
      if (
        username == "admin"
        &&
        password == "pass123"
      ) {
        alert("You are admin")
      }
    }
  }
}
</script>

<style>
</style>
