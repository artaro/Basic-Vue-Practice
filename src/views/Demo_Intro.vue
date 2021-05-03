<template>
  <div id="demo1">
    <h1>Demo1</h1>
    <h1>Demo1: v-model</h1>

    <h1>v-model</h1>
    <!-- MVVM -->
    <input v-model="message" type="text" placeholder="Type here" />
    <!-- interpolation -->
    <div>Yourmessage: {{ message }}</div>
    <button @click="message = ''">Reset Message</button>
    <div>{{ count }}</div>
    <button @click="onClickAdd">add</button>
  </div>
</template>

<script>
export default {
    name: "demo1",
    data() {
    return {
      title: "Test1",
      count: 0,
      message: "",
    };
  },
  methods: {
    onClickAdd() {
      this.count = this.count + 1;
    },
  }
}
</script>

<style></style>
