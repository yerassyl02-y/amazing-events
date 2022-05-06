<template>
  <div @click="goToInner(detail)">
    <p>{{ detail.title }}</p>
    <p>{{ detail.description }}</p>
    <p>{{ detail.price }}</p>
  </div>
</template>

<script>
export default {
  props: {
    details: {
      type: Array,
      default: [],
    },
    detail: {
      type: Object,
      default: {},
    },
  },
  methods: {
    goToInner(detail) {
      this.$router.push({
        path: `/events/${detail.id}`,
      });
    },
  },
};
</script>
