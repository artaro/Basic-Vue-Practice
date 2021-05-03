<template>
  <div id="demo9">
    <ul>
        <h3>v-for</h3>
      <li v-for="(item, index) in ['Angular', 'Vue', 'React']" :key="index">
        {{ item }}
      </li>
    </ul>

    <hr />
    <!-- Array -->
    <ul>
        <h3>v-for array</h3>
      <li v-for="(item, index) in mCourse" :key="index">
        {{ item }}
      </li>
    </ul>
    <hr />
    <!-- Object -->
    <ul>
        <h3>v-for opject</h3>
      <li v-for="(item, index) in mCourse2" :key="index">
        {{ item.title }}, Price {{ item.price }}
      </li>
    </ul>
    <hr/>
    <!-- Short Object -->
    <ul>
        <h3>v-for short object</h3>
      <li v-for="({title, price}, index) in mCourse2" :key="index">
        {{ title }}, Price {{ price }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Demo9",
  data() {
    return {
      mCourse: ["iOS", "Android", "12345"],
      mCourse2: [
        { title: "iOS", price: 10000 },
        { title: "Android", price: 9000 },
      ]
    };
  },
};
</script>

<style></style>
