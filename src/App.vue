<template>
  <input v-model="car.horsePower" />
  <br>

  Plate number 
  <span class="plateNumber">
    {{ car.plateNumber }}
  </span>

  <br>
  Horse power 
  <span class="horsePower">
    {{ car.horsePower }}
  </span>
  <br>

  <span v-if="isCoolCar(car)">
    Ahujenna
  </span>

  <span>Leta masina</span>
</template>

<script>
export default {
  data () {
    return {
      car: {
        plateNumber: "AA-3333",
        horsePower: 1200,
        price: 4000,
      }
    }
  },
  methods: {
    isCoolCar (car) {
      return (car.horsePower > 1000)
    }
  }
}
</script>

<style>
.plateNumber {
  color: red;
  font-weight: bold;
}

.horsePower {
  color: blue;
  font-weight: bold;
}

</style>
