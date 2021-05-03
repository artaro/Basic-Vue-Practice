<template>
  <div id="demo4">
    <h2>{{ firstname }}</h2>
    <h2>{{ lastname }}</h2>
    <h2>{{ fullname }}</h2>
    <h1 style="background-color:gray;">
      Random No from computed property: {{ getrandomno }}
    </h1>
    <h1>Random No from method: {{ getrandomno1() }}</h1>
    <h1>Random No from method : {{ getrandomno1() }}</h1>
    <h1 style="background-color:gray;">
      Random No from computed property: {{ getrandomno }}
    </h1>
    <h1 style="background-color:gray;">
      Random No from computed property: {{ getrandomno }}
    </h1>
    <h1 style="background-color:gray;">
      Random No from computed property: {{ getrandomno }}
    </h1>
    <h1>Random No from method: {{ getrandomno1() }}</h1>
    <h1>Random No from method: {{ getrandomno1() }}</h1>
  </div>
</template>

<script>
export default {
  name: "Demo4",
  methods: {
    getrandomno1() {
      return Math.random();
    },
  },
  data() {
    return {
      firstname: "Tossapol",
      lastname: "Jaidee",
    };
  },
  computed: {
    fullname() {
      return this.firstname + " " + this.lastname;
    },
    getrandomno() {
      return Math.random();
    },
  },
};
</script>

<style></style>
