<template>
    <header>
    <div class="navbar" id="navbar">
      <h1 class="logo">
        <span class="text-primary">
          <i class="fas fa-car">Westcoast</i> Cars
        </span>
      </h1>
      <ul>
        <li><a href="#" class="active">Start</a></li>
        <li><a href="#">Galleri</a></li>
      </ul>
    </div>
  </header>
</template>

<script>
    export default {
        props: [],
        data() {
        }
    }
</script>


<style scoped>
/* Navigation */
.navbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: var(--dark-color);
  opacity: 0.8;
  width: 100%;
  color: var(--light-color);
  height: 4.5rem;
  position: fixed;
  top: 0;
  left: 0;
  padding: 0 2rem;
}

.navbar a {
  color: var(--light-color);
  padding: 0.8rem 0.5rem;
  margin: 0 3px;
}

.navbar a:hover {
  border-bottom: solid 2px var(--primary-color);
}

.navbar ul {
  display: flex;
}

.navbar .logo {
  font-weight: 400;
}

.active {
  border-bottom: solid 2px var(--primary-color);
}

</style>