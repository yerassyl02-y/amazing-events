<template>
  <header class="header">
    <div class="header__wrapper">
      <nuxt-link to="/">
        <img src="@/assets/images/logo_bg.png" />
      </nuxt-link>

      <div class="header__user" @click="dropdown = !dropdown">
        <svg width="30" height="30">
          <use href="@/assets/images/icons.svg#user_logo"></use>
        </svg>
        <span> {{ $auth.user.first_name }}</span>
        <div class="list" v-if="dropdown">
          <div class="list__items">
            <span class="profile" @click="goToProfile">Профиль</span>
          </div>
          <div class="list__items">
            <span class="logout" @click="logout">Выйти</span>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      dropdown: false,
    };
  },
  methods: {
    goToProfile() {
      this.$router.push({
        path: "/profile",
      });
    },
    logout() {
      this.$auth.logout();
      this.$router.push("/login");
    },
  },
};
</script>
