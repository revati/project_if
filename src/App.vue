<template>
  <div v-if="user.isAdmin">
    Es esmu admins
    <b>{{ user.name }}</b>

    <button @click="logout()">Logout</button>
  </div>
  <div v-if="!user.isAdmin">
    Es esmu parasts lietotajs

    <input v-model="user.name">
    <input type="password" v-model="user.pass">

    <button @click="authorize(user.name, user.pass)">Log in</button>
  </div>

  <pre>{{ user | json }}</pre>
</template>

<script>
export default {
  data () {
    return {
      user: {
        name: "",
        pass: "",
        isAdmin: false,
      }
    }
  },
  methods: {
    authorize (username, password) {
      if (username == "admin" && password == "pass123") {
        this.user.isAdmin = true
      } else {
        this.user.pass = ""
      }
    },
    logout () {
      this.user.isAdmin = false
    }
  }
}
</script>

<style>
</style>
