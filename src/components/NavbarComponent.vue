<template>
  <nav class="navbar">
    <h1 class="text-primary">Event Management</h1>
    <div class="navbar-action"></div>
    <BaseButton className="button-primary small" id="sdfsdf">Login</BaseButton>
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
  display: flex;
  justify-content: space-between;
}

@media (max-width: 767px) {
  .navbar {
    padding: 0 1rem;
    width: calc(100vw - 2rem);
  }
}
</style>
