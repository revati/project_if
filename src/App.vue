<template>
  <input type="text" v-model="username"> <br>
  <input type="text"> <br>
  <input type="submit" @click="submit()">
  <div v-if="hasError">
    You must provide data!!! bitch
  </div>
</template>

<script>

export default {
  data () {
    return {
      username: ""
    }
  },
  methods: {
    submit () {
      if(this.username == "suka") {
        alert("fuck off")
      }
    }
  },
  computed: {
    hasError () {
      return this.username.length == 0
    }
  }
}
</script>

<style>
</style>
