<template>
  <div id="app">
    <Header />
    <Content />
    <Footer
      @onClock="onClock"
      title="Code by artaro"
      color="black"
    />
    <div class="clock">{{ time }}</div>
  </div>
</template>

<script>
import Header from "@/components/layout/Header.vue";
import Footer from "@/components/layout/Footer.vue";
import Content from "@/components/layout/Content.vue";
import moment from "moment";

export default {
  name: "app",
  methods: {
    onClock(value) {
      this.time = moment(value).format("MM:DD:YYYY hh:mm:ss");
    },
  },
  data() {
    return {
      time: "",
    };
  },
  components: {
    Header,
    Footer,
    Content,
  },
};
</script>

<style>
.title {
  font-size: 30px;
  color: red;
}
</style>
<style>
.content {
  color: pink;
}
.clock {
  font-size: 12px;
  color: gray;
  text-align: center;
}
</style>
