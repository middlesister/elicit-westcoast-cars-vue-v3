<template>
  <section>Här kommer bilen att finnas</section>
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
            model: 'COrvette',
            modelYear: '2015',
            imageUrl: '',
            mileage: 15000,
            description: ''
        },
      };
    },
  };
</script>
