<template>
  <div id="app">
    <h2>{{name + " " + age}}</h2>
    <p v-for="a in items" :key="a">{{ a }}</p>
    <p v-for="b in price" :key="b" v-if="b > 500">{{b}}</p>
    <p v-on:click="earth">{{name}}</p>
  </div>
</template>
<script>
export default {
  name: "App",
  data() {
    return {
      name: 'Dos',
      age: 55,
      items: ["id", "title"],
      price: [400, 500, 600, 700],
      name: 'Марс',
      earth: 'Земля'
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
