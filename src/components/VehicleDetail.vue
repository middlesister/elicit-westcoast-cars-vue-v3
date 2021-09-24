<template>
  <section class="card">
    <div class="vehicle-item">
      <img v-bind:src="vehicle.imageUrl" alt="" class="thumbnail">
      <div>{{ vehicle.registrationNo }}</div>
      <div>{{ vehicle.make }}</div>
      <div>{{ vehicle.model }}</div>
      <div>{{ vehicle.modelYear }}</div>
      <button 
        v-on:click="onToggleMileage"
        class="btn btn-outline-rounded">{{ displayMileage ? 'Göm' : 'Visa' }} Km</button>
      <div v-if="displayMileage">{{ vehicle.mileage }}</div>
    </div>
  </section>
</template>

<script>
  export default {
    data() {
      return {
        displayMileage: false,
        vehicle: {
            id: 1,
            registrationNo: 'ABC123',
            make: 'Chevrolet',
            model: 'Corvette',
            modelYear: '2015',
            imageUrl: 'https://i.postimg.cc/85xqHwJQ/car3.jpg',
            mileage: 15000,
            description: ''
        },
      };
    },
    methods: {
      onToggleMileage() {
        this.displayMileage = !this.displayMileage;
      },
    }
  };
</script>

<style>
  .vehicle-item {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
  }
</style>