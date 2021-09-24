<template>
  <section class="card">
    <div class="vehicle-item">
      <div>{{ vehicle.registrationNo }}</div>
      <div>{{ vehicle.make }}</div>
      <div>{{ vehicle.model }}</div>
      <div>{{ vehicle.modelYear }}</div>
      <div>{{ vehicle.mileage }}</div>
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
            imageUrl: '',
            mileage: 15000,
            description: ''
        },
      };
    },
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