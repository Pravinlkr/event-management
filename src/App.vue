<template>
  <div id="app">
    <NavbarComponent />
    <router-view />
  </div>
</template>
<script>
import NavbarComponent from "@/components/NavbarComponent.vue";
export default {
  components: {
    NavbarComponent,
  },
};
</script>

<style>
:root {
  --primary-color: #42b983;
  --secondary-color: #86cdad;
  --gray-color: #757575;
  --light-gray-color: #cccccc;
  --border-radius: 14px;
}
body {
  margin: 0;
  padding: 0;
}

a,
.text-primary {
  color: var(--primary-color);
}

.text-secondary {
  color: var(--secondary-color);
}
</style>
