<template>
  <div id="demo11">
    <div>{{ count }}</div>
    <div>{{Math.random()}}</div>
    <button @click="timestamp = Date.now()">Timestamp</button>
    <button @click="count++">Update Count</button>
  </div>
</template>

<script>
export default {
  name: "Demo11",
  created() {
      this.timestamp = 0 //create this var in this function not in data
  },
  mounted() {
    setInterval(() => {
      //this.count++;
      console.log("Timestamp: " + this.timestamp)
    }, 10000);
  },
  data() {
    return {
      count: 0, //local state
    };
  },
};
</script>

<style></style>
