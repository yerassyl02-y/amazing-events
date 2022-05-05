<template>
  <div class="past-events">
    <div class="past-events__wrapper">
      <h2>How it was</h2>
      <div class="past-events__items events">
        <div
          v-for="(event, idx) in past_events"
          :key="idx"
          class="events__event"
        >
          <img :src="event.image" />

          <div class="events__text">
            <h3>
              {{ event.title }}
            </h3>
            <p>{{ event.content }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      past_events: [
        {
          title: "Past Event 1",
          content:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis nisi nisi, auctor quis dictum in, egestas ornare enim. Sed sed volutpat orci. Aliquam cursus varius maximus. Mauris enim justo, dignissim quis suscipit non, suscipit quis massa. Nunc pulvinar vitae magna non sagittis. Integer id nibh a lorem commodo fringilla sit amet non nisi. Cras egestas risus non erat bibendum, eget facilisis arcu porttitor. Ut pretium erat tellus, pulvinar sagittis orci tincidunt non. Donec tempor a magna eu egestas. Sed sit amet nisl maximus, convallis tortor id, pellentesque nulla",
          image: require("@/assets/images/events/image1.jpeg"),
        },
        {
          title: "Past Event 2",
          content:
            "Donec commodo odio ut pellentesque faucibus. Vestibulum metus diam, sodales et eros at, lobortis cursus quam. Ut ligula leo, luctus a risus ac, tempor sollicitudin nunc. Nullam et elementum eros. Morbi quis metus et sapien pretium pharetra a quis metus. Integer non purus auctor, mattis diam ac, viverra nulla. Quisque id blandit nisl, quis sollicitudin elit. Aliquam fermentum in libero vitae lobortis. In eu odio vitae metus pellentesque aliquam.",
          image: require("@/assets/images/events/image3.jpeg"),
        },
        {
          title: "Past Event 3",
          content:
            "Vivamus vehicula sollicitudin odio vitae pulvinar. Proin tempor nisi vel varius imperdiet. Donec vehicula ante in nibh tempus imperdiet. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Vivamus elit nibh, ornare non auctor vel, elementum vitae mi. Fusce egestas nunc eget mi venenatis ullamcorper. Duis quis ultrices magna, quis lobortis diam. Curabitur posuere scelerisque congue. Nunc ultricies quis diam quis volutpat.",
          image: require("@/assets/images/events/image5.jpeg"),
        },
        {
          title: "Past Event 4",
          content:
            "Nunc odio mauris, tristique id felis vitae, commodo tincidunt lorem. Vestibulum euismod venenatis volutpat. Donec molestie dolor at nisl sodales, vel auctor augue maximus. Nunc porta eleifend turpis non iaculis. Etiam scelerisque nibh ut ante tempor, a fermentum neque bibendum. Vivamus pharetra tortor ut felis lobortis, ut luctus lacus euismod. Donec vitae arcu euismod, varius mi sed, bibendum arcu. Sed ac risus sed odio accumsan elementum. Cras nisi ipsum, volutpat quis orci eget, imperdiet elementum massa. Quisque ac velit dapibus, interdum nulla ac, venenatis magna. ",
          image: require("@/assets/images/events/image7.jpeg"),
        },
        {
          title: "Past Event 5",
          content:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur non leo pretium, posuere metus eu, convallis lectus. Nam augue leo, aliquet vitae malesuada ac, placerat sit amet metus. Cras non lacinia nisi. Morbi interdum cursus dui ac varius. Nam nec fermentum dui, a sodales ex. In ut felis eu turpis suscipit posuere. Praesent dictum eu tellus non facilisis. Praesent iaculis tortor ac leo efficitur, a bibendum lectus volutpat. Pellentesque rutrum viverra tempor. Etiam molestie elementum ex ac tincidunt. Integer elementum nisl vitae cursus eleifend. ",
          image: require("@/assets/images/events/image8.jpeg"),
        },
      ],
    };
  },
};
</script>

<style>
</style>