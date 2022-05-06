<template>
  <div class="events-page">
    <div class="events-page__wrapper">
      <div class="events-page__headers">
        <span v-for="(header, idx) in headers" :key="idx">{{
          header.title
        }}</span>
      </div>
      <div class="events-page__details">
        <events-list
          v-for="(detail, idx) in details"
          :details="details"
          :key="idx"
          :detail="detail"
        />
      </div>
    </div>
  </div>
</template>

<script>
import EventsList from "../../components/EventsList.vue";
export default {
  components: { EventsList },
  data() {
    return {
      headers: [
        {
          title: "Type",
        },
        {
          title: "Description",
        },
        {
          title: "Price",
        },
      ],
      details: [
        {
          title: "Concert",
          description: "Singeres, Actors, Animators",
          price: "50.00",
          id: 1,
        },
        {
          title: "Fashoin Show",
          description: "Models, Actors, Animators",
          price: "70.00",
          id: 2,
        },
        {
          title: "Party",
          description: "Singers, Actors, Animators, DJ",
          price: "80.00",
          id: 3,
        },
        {
          title: "Wedding",
          description: "Singers, Actors, Animators, DJ, Host",
          price: "100.00",
          id: 4,
        },
        {
          title: "Kids Show",
          description: "Actors, Animators",
          price: "80.00",
          id: 5,
        },
        {
          title: "Theatre Show",
          description: "Actors, Animators",
          price: "90.00",
          id: 6,
        },
        {
          title: "Club Show",
          description: "Singers, Actors, Animators, DJ, Barman",
          price: "95.50",
          id: 7,
        },
      ],
    };
  },
};
</script>
