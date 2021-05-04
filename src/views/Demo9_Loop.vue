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
    <hr />
    <!-- Short Object -->
    <ul>
      <h3>v-for short object</h3>
      <li v-for="({ title, price }, index) in mCourse2" :key="index">
        {{ title }}, Price {{ price }}
      </li>
    </ul>

    <!-- Dynamic add and remove-->
    <ul>
      <h3>Dynamic add and remove</h3>
      <input type="text" placeholder="Title" v-model="course.title" />
      <br />
      <input type="number" placeholder="Price" v-model="course.price" />
      <br>
      <button @click="addCourse">Submit</button>

      <li v-for="(course, index) in dynamicCourses" :key="index">
        {{ course.title }}, Price {{ course.price }}
        <button @click="removeCourse(index)">X</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Demo9",
  methods: {
    addCourse() {
      this.dynamicCourses.push(this.course);
      this.course = {title: "", price: 0}
    },
    removeCourse(index){
      this.dynamicCourses.splice(index, 1)
    },
  },
  data() {
    return {
      course: { title: "", price: 0 },
      mCourse: ["iOS", "Android", "12345"],
      mCourse2: [
        { title: "iOS", price: 10000 },
        { title: "Android", price: 9000 },
      ],
      dynamicCourses: [],
    };
  },
};
</script>

<style></style>
