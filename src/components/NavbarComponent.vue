<template>
  <nav class="navbar">
    <h1 class="text-primary">Event Management</h1>
    <!-- <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> -->
  </nav>
</template>

<script>
export default {};
</script>

<style scoped>
.navbar {
  padding: 0 2rem;
  width: calc(100vw - 4rem);
  border-bottom: 1px solid var(--primary-color);
}

@media (max-width: 767px) {
  .navbar {
    padding: 0 1rem;
    width: calc(100vw - 2rem);
  }
}
</style>
