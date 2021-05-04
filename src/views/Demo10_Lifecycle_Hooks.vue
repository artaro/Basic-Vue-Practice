<template>
  <div id="demo10">
    <h1>Lifecycle Hooks</h1>
    <span style="color:gray;">#Open console to see what is happening</span>
    <br/>
    <span>{{counter}}</span>
    
    <br/>
    <button @click="add">Change</button>
  </div>
</template>

<script>
export default {
  name: "Demo10",
  data() {
    return {
      counter: 0,
    };
  },
  methods: {
    add() {
      this.counter++;
    },
  },
  beforeCreate() {
    console.log("Created");
  },
  created() {
    console.log("Created");
  },
  mounted() {
    console.log("Mouted");
  },
  beforeUpdate() {
    console.log("beforeUpdate");
  },
  updated() {
    console.log("updated");
  },
  beforeDestroy() {
    console.log("beforeDestroyed");
  },
  destroyed() {
    console.log("Destroyed");
  },
};
</script>

<style>
</style>
