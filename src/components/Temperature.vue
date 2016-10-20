<template>
  <div>
    <span v-if="temeratureFormat == 'celsisus'">{{ temperature }}</span>
    <span v-if="temeratureFormat == 'farenheit'">{{ celsiusToFarenheit(temperature) }}</span>
  </div>
</template>

<script>
export default {
  props: ['temperature', 'temeratureFormat'],
  methods: {
    celsiusToFarenheit: temp => {
      if(temp.isInt) {
        return temp * 1.8 + 32
      }

      return "Fuck off"
    }
  }
}
</script>

<style>
</style>
