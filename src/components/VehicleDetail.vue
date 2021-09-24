<template>
  <section class="card">
    <div class="vehicle-item">
      <img v-bind:src="imageUrl" alt="" class="thumbnail">
      <div>{{ registrationNo }}</div>
      <div>{{ make }}</div>
      <div>{{ model }}</div>
      <div>{{ modelYear }}</div>
      <button 
        v-on:click="onToggleMileage"
        class="btn btn-outline-rounded">{{ displayMileage ? 'Göm' : 'Visa' }} Km</button>
      <div v-if="displayMileage">{{ mileage }}</div>
    </div>
  </section>
</template>

<script>
  export default {
    props: [
      'id',
      'imageUrl',
      'registrationNo',
      'make',
      'model',
      'modelYear',
      'mileage',
      'description',
    ],
    data() {
      return {
        displayMileage: false,
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