<template>
  <h1 id="app1" v-on:mousemove="getConsole()">Home Component {{ message }}</h1>
  <!-- <button v-on:click="test()">Click Me</button> -->
  <input type="text" v-model="count" />
 
  <h1>{{ count }}</h1>
   
  <input type="text" placeholder="Name" v-model="name" />
  <input type="text" placeholder="email" v-model="email" />
  <button type="submit" v-on:click="getClick()">Submit</button>

 <br/><br/>
    <label for="java">java</label>
    <input type="checkbox" value="java" id="java" v-model="technology" />

    <label for="node">node</label>
    <input type="checkbox" value="node" id="node" v-model="technology" />

    <label for="javascript">javascript</label>
    <input type="checkbox" value="javascript" id="javascript" v-model="technology" />
    <p>{{technology}}</p>


       <h2>radio button</h2>
      <label for="student">javascript</label>
    <input type="radio" value="student" name="profession" id="student"  />

    <label for="developer">developer</label>
    <input type="radio" value="developer" name="profession" id="developer"/>

    <h1>If else</h1>
    <p v-if="show">if condition</p>
     <p v-else>else condition</p>

     <h1>Toggle</h1>
     <p v-if="display">if condition</p>
      <p v-else>else condition</p>
     <button v-on:click="display=!display">toggle</button>
     <br/><br/>
<h1>For loop in vue</h1>
<ul>
    <li v-for="item in tech" :key="item" >{{item}}</li>
</ul>
<br/><br/>
<ul>
    <li v-for="item in user" :key="item.name" >name is:{{item.name}}  email is: {{item.email}}</li>
</ul>
<br/><br/>
<h1>Using ref</h1>
<input type="text" ref="input" />
<button v-on:click="getData">Click me</button>
<br/><br/>
<h1>Slots</h1>
<Child>
  <h1>slots are passing</h1>
</Child>
<br/><br/>
<h1>Multiple Slots</h1>


</template>
  
  <script>
import Child from './Child.vue'
export default {
  components: { Child },
  name: "Home",
  data() {
    return {
      count: 0,
      name: null,
      email: null,
      technology:[],
      show:true,
      display:true,
      tech:['java','javascript','react','view'],
      user:[
        {
            name:"astha",
            email:"astha1232gmail"
        },
         {
            name:"sana",
            email:"sana1232gmail"
        }
      ]
    };
  },
  methods: {
    getClick() {
      console.warn("clicked :", this.name, this.email);
    },
    test() {
      this.count = this.count + 1;
    },
    getConsole() {
      console.warn("function called");
    },
    getData(){
      this.$refs.input.focus()
      let val=this.$refs.input.value
      console.warn(val)
    }
  },
};
</script>
  
<style scoped>
h1 {
  color: red;
  margin-top: -13px;
}
h2 {
  color: rgb(8, 0, 255);
  margin-top: 13px;
}


</style>



