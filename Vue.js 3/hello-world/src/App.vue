<template>
  <h1>{{ greet }}</h1>
  <h1>My name is {{ name }}</h1>
  <h1>{{ greet }} {{ name }}</h1>
  <h1>{{ channel }}</h1>
  <h1 v-html="channel"></h1>
  <h1 v-html="hack"></h1>
  <h1 v-text="gender"></h1>
  <h1 v-text="name"></h1>
  <!-- <h1 v-text="chanel"></h1> -->
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      greet: "Hello Charming Man",
      name: "Karan Singh",
      gender: "Male",
      channel: "<b>YouTube</b>",
      hack: `<a href="#" onclick="alert('You have been Hacked!')">Win a Prize!</a>`,
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
