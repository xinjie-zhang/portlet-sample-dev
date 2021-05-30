<template>
  <div id="app">
    <template v-for="block in content.body">
      <component :is="block.component" :block="block" :key="block._uid"></component>
    </template>
  </div>
</template>

<script>
import Bar from "./components/Bar";
import Foo from "./components/Foo";

export default {
  data() {
    return {
      content: {
        body: [
          {
            _uid: "BUY6Drn9e1",
            component: "foo",
            headline: "Foo"
          },
          {
            _uid: "gJZoSLkfZV",
            component: "bar",
            title: "Bar"
          },
          {
            _uid: "X1JAfdsZxy",
            component: "foo",
            headline: "Another headline"
          }
        ]
      }
    };
  },
  name: "App",
  components: {
    Bar,
    Foo
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
