<template>
  <h1>Parent component</h1>
  <Child name="hii my name is astha" :user="user" :getdata="getdata" />
  <ul>
    <li v-for="item in users" :key="item.name">
      <Child :data="item" />
    </li>
  </ul>
</template>

<script>
import Child from "./Child.vue";
export default {
  name: "home",
  components: {
    Child,
  },
  data() {
    return {
      user: {
        name: "sandhya",
        email: "sandhya@123",
      },
      users: [
        {
          name: "sandhya",
          email: "sandhya@123",
        },
        {
          name: "astha",
          email: "asthaa@123",
        }
      ],
    }
  },
  methods: {
    getdata() {
      alert("button clicked");
    },
  },
};
</script>