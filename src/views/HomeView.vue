<template>
  <div class="home">
    <img src="@/assets/events.svg" alt="event image" />
    <h2 class="text-primary">Manage Your Events At One Place</h2>
    <div>
      To get started
      <router-link to="/login">Login</router-link>
      or
      <router-link to="/register">Register</router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeView",
};
</script>

<style scoped>
.home {
  text-align: center;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.home img {
  height: 15rem;
}
</style>
