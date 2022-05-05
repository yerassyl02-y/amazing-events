<template>
  <header class="header">
    <div class="header__wrapper">
      <img src="@/assets/images/logo_bg.png" />

      <div class="header__user" @click="goToProfile">
        <svg width="30" height="30">
          <use href="@/assets/images/icons.svg#user_logo"></use>
        </svg>
        <span> {{ $auth.user.first_name }}</span>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  methods: {
    goToProfile() {
      this.$router.push({
        path: "/profile",
      });
    },
  },
};
</script>
