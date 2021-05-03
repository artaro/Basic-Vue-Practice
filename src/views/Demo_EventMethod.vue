<template>
  <div id="demo2">
    <h1>Event and Method</h1>
    <!-- Method v-on:click -->
    <button v-on:click="clickMe">Click Me</button>
    <!-- Method v-on:click with sending variables -->
    <button v-on:click="clickMe2('Welcome To My Basic Vue')">Click Me 2</button>
    <!-- Method @click with sending variables -->
    <button @click="clickMe3('Another Welcome To My Basic Vue')">
      Click Me 3
    </button>
    <!-- Return Method Timestamp -->
    <h3>{{ getTimestamp() }}</h3>
  </div>
</template>

<script>
export default {
  name: "Demo2",
  mounted() {
    this.initial();
  },
  methods: {
    initial() {
      console.log("Initialization");
    },
    clickMe() {
      alert("Hi");
    },
    clickMe2(message) {
      alert(message);
    },
    clickMe3(message) {
      alert(message);
    },
    getTimestamp() {
      return Date();
    },
  },
};
</script>

<style></style>
