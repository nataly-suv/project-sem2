<template>
  <div id="app">

    <Task1Sem2 />
    <Task2Sem2 />
    <Task3Sem2 />
    <HomeWork1/>
  </div>
</template>

<script>
import HomeWork1 from './components/HomeWork1.vue';

import Task1Sem2 from "./components/Task1.vue";
import Task2Sem2 from "./components/Task2.vue";
import Task3Sem2 from "./components/Task3.vue";

export default {
  name: "App",
  components: {
    // HelloWorld,
    Task1Sem2,
    Task2Sem2,
    Task3Sem2,
    HomeWork1,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-size: 30px;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
