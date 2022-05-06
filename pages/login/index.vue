<template>
  <div class="login">
    <div class="login__wrapper">
      <div class="login__form form">
        <h2>Авторизация</h2>
        <input type="tel" v-model="login.phone_number" />
        <div class="form__password">
          <input type="password" v-model="login.password" />
          <span>Забыли пароль?</span>
        </div>

        <button @click="sendData" class="btn">Войти</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  layout: "login",
  data() {
    return {
      login: {
        phone_number: "",
        password: "",
      },
    };
  },
  methods: {
    async sendData() {
      try {
        const res = await this.$auth.loginWith("local", {
          data: this.login,
        });
        if (res.status < 400) {
          this.$router.push({
            path: "/",
          });
        }
      } catch (err) {
        console.error(err);
      }
    },
  },
};
</script>
