<template>
  <div id="demo12">
    <h1 ref="title">
      Waiting for changes
    </h1>
    <input type="text" ref="input1" placeholder="This will be focused" />
  </div>
</template>

<script>
export default {
  name: "Demo12",
  mounted() {
    this.$refs["title"].textContent = "Welcome to my practice vue";
    this.$refs["input1"].focus();
    this.$refs["input1"].value = "12345";
  },
};
</script>

<style></style>
