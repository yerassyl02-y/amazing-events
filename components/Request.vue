<template>
  <div class="request">
    <div class="request__dialog">
      <h2>Do you want to present your own event? Send us your request.</h2>
      <div class="request__inputs inputs">
        <div class="inputs__personal">
          <input
            v-for="(input, idx) in inputs"
            :key="'A' + idx"
            :placeholder="input.placeholder"
          />
        </div>
        <div class="inputs__additional">
          <input placeholder="Which type of event do you want?" />
          <div class="selector" :class="{ opened: opened == true }">
            <div class="selector__selected" @click="opened = !opened">
              <span>{{ selected }}</span>
            </div>
            <div v-if="opened" class="selector__items">
              <div
                v-for="(item, idx) in items"
                :key="'B' + idx"
                @click="choseItem(item)"
              >
                <span>{{ item.count }}</span>
              </div>
            </div>
          </div>
          <textarea placeholder="Write your comments here..." />
        </div>
      </div>
      <button @click="openDialog" class="green-btn">Send</button>
    </div>
    <v-dialog v-model="dialog">
      <h1>Thanks! Your request will be processed!</h1>
      <svg width="143" height="142">
        <use href="@/assets/images/icons.svg#success"></use>
      </svg>
      <svg width="14" height="14" class="close" @click="closeDialog">
        <use href="@/assets/images/icons.svg#close"></use>
      </svg>
      <span @click="closeDialog">back to the home page</span>
    </v-dialog>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selected: "50 people",
      opened: false,
      dialog: false,
      inputs: [
        {
          placeholder: "Name",
        },
        {
          placeholder: "Surname",
        },
        {
          placeholder: "E-mail",
        },
      ],
      items: [
        {
          count: "50 people",
        },
        {
          count: "100 people",
        },
        {
          count: "200 people",
        },
        {
          count: "More than 200 people",
        },
      ],
    };
  },
  methods: {
    choseItem(item) {
      this.selected = item.count;
    },
    openDialog() {
      this.dialog = true;
    },
    closeDialog() {
      this.dialog = false;
    },
  },
};
</script>

<style>
</style>