<template>

  <div id="app">
    <h1>Lesson 2</h1>

    <!-- One РЕШЕНА -->
    <div class="one" v-for="a in searcher" :key="a" v-on:click="searchTitle(a)">
      {{a.title}}
    </div>

    <!-- Two НЕ РЕШЕНА-->
    <div class="two" style="margin-top: 20px;">
      <input type="text">
      <button v-on:click="showInputText">Button</button>
      <p>{{ username }}</p>
    </div>

    <!-- Three НЕ РЕШЕНА -->
    <div class="three" style="margin-top: 20px;">
      <input type="text" v-bind:value="search" v-on:input="showInputType">
      <p>{{ search }}</p>
    </div>

    <!-- Four НЕ РЕШЕНА -->
    <div class="four" style="margin-top: 20px;">
      <div v-for="a in lists" :key="a">{{ a }}</div>
      <button v-on:click="addElement">Button</button>
    </div>

    <!-- Five НЕ РЕШЕНА -->
    <div class="five" style="margin-top: 20px;">
      <input type="text" v-bind:input="inputText" v-on:="">
      <p>Я невидимый</p>
    </div>
  </div>

</template>

<script>

export default {
  name: "App",

  data() {
    return {
      searcher: [
        {
          id: 1,
          title: "google"
        },
        {
          id: 2,
          title: "yandex"
        }
      ],

      username: "",

      search: "",

      lists: [],
    }
  },

  methods: {
    searchTitle(a) {
      return console.log(a.title);
    },

    showInputType(event) {
      console.log(event.target.value);
      this.search = event.target.value;
    },

    addElement() {
      this.lists.push('я vue разработчик')
    }
  }
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
