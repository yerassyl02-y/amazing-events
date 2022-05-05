<template>
  <div class="homepage">
    <events />
    <hr class="hr" />
    <news />
    <hr class="hr" />
    <past-events />
    <h2>Our partners</h2>
    <partners />
    <hr class="hr" />
    <request />
  </div>
</template>

<script>
import Events from "../components/Events.vue";
import News from "../components/News.vue";
import Partners from "../components/Partners.vue";
import PastEvents from "../components/PastEvents.vue";
import Request from "../components/Request.vue";
export default {
  components: { Events, News, PastEvents, Partners, Request },
  middleware: ["auth"],
};
</script>

<style lang="scss" scoped>
.homepage {
  max-width: 1160px;
  width: 100%;

  border-top-left-radius: 20px;
  border-top-right-radius: 20px;

  margin: 0 auto;

  padding: 100px 0;

  background: #359866;
  opacity: 0.9;
}
.hr {
  max-width: 1100px;
  width: 100%;

  margin: 30px auto;

  color: white;
}
h2 {
  margin: 10px 0 !important;
  width: 100%;
  text-align: center;
  font-weight: bold;
}
</style>
