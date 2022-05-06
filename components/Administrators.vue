<template>
  <div class="administrators">
    <p>{{ item.first_name }}</p>
    <p>{{ item.second_name }}</p>
    <p>{{ item.phone_number }}</p>
    <p>{{ item.address }}</p>
    <p>{{ item.email }}</p>

    <div class="administrators__icons icons">
      <svg width="14" height="14" @click="openDialog">
        <use href="@/assets/images/icons.svg#delete"></use>
      </svg>
    </div>
    <v-dialog v-model="dialog">
      <h1>Are you sure you want to delete the administrator?</h1>
      <svg width="143" height="142">
        <use href="@/assets/images/icons.svg#delete_user"></use>
      </svg>
      <svg width="14" height="14" class="close_btn" @click="closeDialog">
        <use href="@/assets/images/icons.svg#close"></use>
      </svg>
      <div class="buttons">
        <button @click="deleteUser(item)">Delete</button>
        <span> go back to the list </span>
      </div>
    </v-dialog>
  </div>
</template>

<script>
export default {
  props: {
    administrators: {
      type: Array,
      default: [],
    },
    item: {
      type: Object,
      default: {},
    },
  },
  data() {
    return {
      dialog: false,
    };
  },
  methods: {
    openDialog() {
      this.dialog = true;
    },
    deleteUser(item) {
      this.$emit("deleteUser", item);
      this.dialog = false;
    },
    closeDialog() {
      this.dialog = false;
    },
  },
};
</script>
