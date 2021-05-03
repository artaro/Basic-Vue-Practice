<template>
  <div id="demo6">
    <!-- when click submit and press ok form will clear-->
    <form v-on:submit.prevent="submit">
      <div>
        <label for="first_name">Firstname</label>
        <input type="text" name="first_name" v-model.trim="applicant.first_name" />
      </div>

      <div>
        <label for="first_name">Lastname</label>
        <!-- lazy not update until click another form or submit then show-->
        <input type="text" name="first_name" v-model.lazy="applicant.last_name" />
      </div>

      <div>
        <label for="sex">Male</label>
        <input type="radio" name="sex" value="male" v-model="applicant.sex" />

        <label for="sex">Female</label>
        <input type="radio" name="sex" value="female" v-model="applicant.sex" />
      </div>
      <div>
        <label for="age">Age:</label>
        <input type="number" v-model.number="applicant.age" />
      </div>

      <div>
        <select name="course" v-model="applicant.course">
          <option value="React">React</option>
          <option value="Vue">Vue</option>
          <option value="Angular">Angular</option>
        </select>
      </div>
      <button type="submit">Submit</button>
      <!-- if normal press clear will clear but if alt with press will use default-->
      <button type="button" @click.exact="clear" @click.alt="useDefault">Clear</button>
    </form>
    <div style="margin-top: 16px; color: red;">
      #Spy {{ JSON.stringify(applicant) }}
    </div>
  </div>
</template>

<script>
export default {
  name: "Demo6",
  data() {
    return {
      applicant: {
        first_name: "",
        last_name: "",
        sex: "male",
        course: "Vue",
        age: 0
      },
    };
  },
  methods: {
    submit() {
      //event.preventDefault();

      alert(JSON.stringify(this.applicant));
    },
    clear() {
      this.applicant = {
        first_name: "",
        last_name: "",
        sex: "male",
        course: "Vue",
        age: 0,
      };
    },
    useDefault() {
      this.applicant = {
        first_name: "UNKNOWN",
        last_name: "UNKNOWN",
        sex: "male",
        course: "Vue",
        age: 0,
      };
    },
  },
};
</script>

<style></style>
