<template>
  <h1>{{ greet }}</h1>
  <h1>My name is {{ name }}</h1>
  <h1 v-text="gender"></h1>
  <h1 v-text="name"></h1>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      greet: "Hello Charming Man",
      name: "Karan Singh",
      gender: "Male",
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
