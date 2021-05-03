<template>
  <div>
    <h1>Data</h1>
    <button @click="count++">Count ++</button>
    <div>
      <span>{{ count }}</span>
    </div>
    <div>{{ message }}</div>
    <div>{{ isLogged }}</div>
    <h1>Try to delete message in the box</h1>
    <input type="text" placeholder="Enter Message" v-model="message" />
    <div>
      <h1>Try this button to see a message</h1>
      <button @click="isLogged = true">Try Here</button>

      <h2 v-if="isLogged">Yeah !</h2>
    </div>
    <div>
      <h1>Dictionary</h1>
      {{ account }}
    </div>
    <div>
      <h1>My Fav Heroes In DOTA2</h1>
      {{ heroes }}
      <ul>
        <li v-for="(item, index) in heroes" :key="index">
          {{ index + 1 }}. {{ item }}
        </li>
      </ul>
      <span class="title"> test global style </span>
      <span class="content"> test another global style from app</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "Demo3",
  mounted() {
    this.message = "Welcome Again !";
  },
  data() {
    return {
      count: 0,
      message: "",
      isLogged: false,
      account: {
        username: "admin",
        password: "1234",
      },
      heroes: [
        "Morphing",
        "Ember Spirit",
        "Storm Spirit",
        "Void Spirit",
        "Templar Assassin",
        "Invoker",
        "Queen Of Pain",
      ],
    };
  },
};
</script>

<style scoped>
li {
  color: cyan;
}
.title {
  color: cyan;
}
</style>
