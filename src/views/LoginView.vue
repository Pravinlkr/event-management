<template>
  <div class="loginContainer">
    <div class="login-image">
      <img src="@/assets/lock.svg" alt="lock image" />
    </div>
    <div class="formContainer">
      <BaseInput
        label="Email"
        type="email"
        placeholder="Enter email"
        v-model="credentials.email"
        :value="credentials.email"
        class="mb-8"
        :showIcon="true"
        :isRequired="true"
      >
        <template v-slot:icon>
          <img src="@/assets/input.svg" alt="event image" />
        </template>
      </BaseInput>
      <BaseInput
        label="Password"
        type="password"
        placeholder="Enter password"
        v-model="credentials.password"
        :value="credentials.password"
        class="mb-8"
        :showIcon="true"
        :isRequired="true"
      >
        <template v-slot:icon>
          <img src="@/assets/input.svg" alt="event image" />
        </template>
      </BaseInput>
      <div class="loginActionBox">
        <BaseButton className="button-primary small" type="submit">
          Login</BaseButton
        >
        <router-link to="/register">Create New Account</router-link>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      credentials: {
        email: "",
        password: "",
      },
    };
  },
};
</script>
<style scoped>
.loginContainer {
  height: 400px;
  width: 400px;
  border: 1px solid var(--primary-color);
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  border-radius: var(--border-radius);
}

.login-image {
  position: absolute;
  top: -40px;
  left: 170px;
  width: 50px;
  height: 50px;
  border: 1px solid var(--primary-color);
  background-color: white;
  border-radius: 50%;
  padding: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.login-image img {
  height: 40px;
  width: 40px;
}

.formContainer {
  margin: 6rem 2rem;
}

.mb-8 {
  margin-bottom: 32px;
}
.loginActionBox {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
@media (max-width: 767px) {
  .loginContainer {
    height: 400px;
    width: calc(100vw - 2rem);
  }
  .login-image {
    left: calc(((100vw - 2rem) / 2) - 30px);
  }
}
</style>
