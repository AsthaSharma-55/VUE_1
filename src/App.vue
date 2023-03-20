<script setup>
//import HelloWorld from './components/HelloWorld.vue'
import HomeVue from './components/Home.vue'
import TheWelcome from './components/TheWelcome.vue'
import Home from './components/Home.vue'
import parent from './components/partent.vue'
import classbinding from './components/classbinding.vue'
import Form from './components/Form.vue'
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div>
      <!-- <HelloWorld msg="Hello world" /> -->
      <!-- <Form/> -->
      <Home/>
      <!-- <parent/> -->
      <!-- <classbinding/> -->
    </div>
  </header>

  <main>
   
  </main>
</template>
<script>
 import { createApp } from 'vue'

  createApp({
    data() {
      return {
        message: 'Hello Vue!'
      }
    }
  }).mount('#app1')

</script>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
