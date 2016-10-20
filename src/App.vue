<template>
  <div>
    <input v-model="temperature">
    <br>
    <input 
      id="farenheit"
      type="radio" 
      v-model="temeratureFormat" 
      value="farenheit">
    <label for="farenheit">Farenheit</label>
    <input 
      id="celsisus"
      type="radio" 
      v-model="temeratureFormat" 
      value="celsisus">
    <label for="celsisus">Celsius</label>


    <br>
    <temperature 
      :temerature-format="temeratureFormat" 
      :temperature="temperature">
    </temperature>

    <br>
    <temperature 
      :temerature-format="temeratureFormat" 
      :temperature="temperature">
    </temperature>

    <br>
    <temperature 
      :temerature-format="temeratureFormat" 
      :temperature="temperature">
    </temperature>
  </div>
</template>

<script>
import Temperature from './components/Temperature'

export default {
  data () {
    return {
      temeratureFormat: "farenheit",
      temperature: 32,
    }
  },
  components: {
    Temperature
  }
}
</script>

<style>
</style>
