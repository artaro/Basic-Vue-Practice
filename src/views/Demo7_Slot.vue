<template>
  <div id="Demo7">
    <Clock>
      <span style="color:red">Current time: </span>
    </Clock>
    <Clock>
      <span style="color:teal">Current time: </span>
    </Clock>
    <!-- Fallback content -->
    <Clock/>

    <Clock>
      <span>TEST</span>
      <br>
      <template v-slot:header>
        <h1>Header</h1>
      </template>
      <template v-slot:footer>
        <h3>Footer</h3>
      </template>
    </Clock>
  </div>
</template> 

<script>
import Clock from "@/components/helpers/Clock.vue";
export default {
  name: "Demo7",
  components: {
    Clock,
  },
};
</script>

<style></style>
