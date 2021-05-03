<template>
  <div id="demo5">
    <!-- bind url -->
    <img v-bind:src="imageUrl" v-bind:height="height" />
    <br />
    <a v-bind:href="linkUrl">Go Google</a>
    <!-- bind style array -->
    <div :class="[false ? error : '', important]">Click</div>
    <!-- bind style -->
    <div :style="{ color, fontSize }">Binding Style</div>
    <!-- bind style object-->
    <div :style="isActive ? styleObj : ''">Another Binding Style</div>
    <!-- toggle style -->
    <button @click="isActive = !isActive">ToggleActive</button>
  </div>
</template>

<script>
export default {
  name: "Demo5",
  data() {
    return {
      imageUrl:
        "https://thenextscoop.com/wp-content/uploads/2018/01/Free-of-Charge-Logos.jpg",
      height: 100,
      linkUrl: "https://google.com",
      error: "error_class",
      important: "important",
      color: "green",
      fontSize: "90px",
      styleObj: {
        backgroundColor: "cyan",
        color: "white",
      },
      isActive: false,
    };
  },
};
</script>

<style>
.error_class {
  background-color: red;
  color: white;
}
.important {
  font-weight: 900;
}
</style>
