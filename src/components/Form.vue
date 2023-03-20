<template>
  <div>
   
    <ul>
      <li v-for="item in error" v-bind:key="item">{{item}} not valid</li>
    </ul>
    <form>
      <label>Email:</label>
      <input type="text" placeholder="Enter Email" v-model="form.email" />

      <br /><br />

      <label>password:</label>
      <input
        type="password"
        placeholder="Enter password"
        v-model="form.password"
      />

      <br /><br />

      <select v-model="form.country">
        <option>India</option>
        <option>USA</option>
        <option>China</option>
      </select>
      <br /><br />

      <h4>technology</h4>
      <label>java:</label>
      <input type="checkbox" value="java" v-model="form.technology" />
      <label>.net:</label>
      <input type="checkbox" value=".net" v-model="form.technology" />
      <br /><br />

      <h4>gender</h4>
      <label>Male:</label>
      <input type="radio" value="male" name="gender" v-model="form.gender" />
      <label>Female:</label>
      <input type="radio" value="female" name="gender" v-model="form.gender" />
      <br /><br />

      <button v-on:click="getData" type="button">Submit</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "Form",
  data() {
    return {
      form: {
        email: " ",
        password: "",
        country: "",
        technology: [],
        gender: "",
      },
    };
  },
  methods: {
    getData() {
      this.error = [];
      for (const item in this.form) {
        if (this.form[item] === "" || this.form[item].length === 0) {
          this.error.push(item);
        }
      }
      if (this.error.length === 0) {
        alert("data has been submitted");
      }
      console.warn("form", this.form, this.error);
    },
  },
};
</script>