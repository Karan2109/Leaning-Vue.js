<template>
  <h1>{{ greet }}</h1>
  <h1>My name is {{ name }}</h1>
  <h1>{{ greet }} {{ name }}</h1>
  <h1>{{ channel }}</h1>
  <h1 v-html="channel"></h1>
  <h1 v-html="hack"></h1>
  <h1 v-text="gender"></h1>
  <h1 v-text="name"></h1>
  <h2 v-bind:id="headingId">Heading</h2>
  <button v-bind:disabled="isDisabled">Bind</button>
  <h2 class="underline">Underlined Text</h2>
  <h2 class="underline" v-bind:class="status">Status</h2>
  <h2 v-bind:class="isPromoted && `promoted`">Promoted Movie</h2>
  <h2 v-bind:class="isSoldout ? 'sold-out' : 'new'">soldout? Movie</h2>
  <h2 v-bind:class="['new', 'promoted']">Newly Promoted Movie</h2>
  <h2 v-bind:class="[isPromoted && 'promoted', isSoldout ? 'sold-out' : 'new']">
    Array conditional movie
  </h2>
  <h2
    v-bind:class="{
      promoted: isPromoted,
      new: !isSoldout,
      'sold-out': isSoldOut,
    }"
  >
    Object conditional movie
  </h2>
  <h2
    v-bind:style="{
      color: highLightColor,
      fontSize: headerSize + 'px',
      padding: '20px',
    }"
  >
    Inline styling
  </h2>

  <h2 v-bind:style="headerStyleObject">Style using Object</h2>

  <div v-bind:style="[baseStyleObject, successStyleObject]">Success Style</div>

  <div v-bind:style="[baseStyleObject, danderStyleObject]">Danger Style</div>
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
      headingId: "heading",
      isDisabled: true,
      status: "Success",
      isPromoted: true,
      isSoldOut: true,
      highLightColor: "Orange",
      headerSize: 50,
      headerStyleObject: {
        color: "cyan",
        fontSize: "50px",
        padding: "20px",
      },
      baseStyleObject: {
        fontSize: "50px",
        padding: "10px",
      },
      successStyleObject: {
        color: "green",
        backgroundColor: "lightgreen",
        border: "1px solid green",
      },
      danderStyleObject: {
        color: "darkred",
        backgroundColor: "lightcoral",
        border: "1px solid darkred",
      },
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

.underline {
  text-decoration: underline;
}

.promoted {
  font-style: italic;
  /* color: green; */
}

.new {
  color: green;
}

.sold-out {
  color: red;
}
</style>
