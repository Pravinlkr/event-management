<template>
  <div>
    <button v-on="$listeners" class="button" v-bind="$attrs" :class="className">
      <slot></slot>
    </button>
  </div>
</template>

<script>
export default {
  inheritAttrs: false,
  props: {
    className: {
      type: String,
    },
  },
};
</script>

<style scoped>
.button {
  display: inline-flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 2rem;
  height: 50px;
  border-radius: calc(var(--border-radius) / 2);
  background: transparent;
  border: none;
  text-align: center;
  font-weight: 600;
  white-space: nowrap;
  transition: all 0.2s linear;
  cursor: pointer;
}

button.button-primary {
  background-color: var(--primary-color);
  color: white;
}
button.small {
  height: 35px;
}
button.outlined {
  border: 1px solid var(--primary-color);
  background: transparent;
  color: var(--primary-color);
}
</style>
