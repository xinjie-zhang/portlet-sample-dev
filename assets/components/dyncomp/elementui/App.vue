<template>
  <div id="app">
  ElementUI
    <template v-for="block in content.body">
      <component :is="block.component" :block="block" :key="block._uid"></component>
    </template>
  </div>
</template>

<script>
import TextInput from "./components/TextInput";
import SelectInput from "./components/SelectInput";

export default {
  data() {
    return {
      content: {
        body: [
          {
            _uid: "BUY6Drn9e1",
            component: "TextInput",
            title: "Foo"
          },
          {
            _uid: "gJZoSLkfZV",
            component: "select-input",
            headline: "Bar"
          },
          {
            _uid: "X1JAfdsZxy",
            component: "text-input",
            title: " headline"
          }
        ]
      }
    };
  },
  name: "App",
  components: {
    TextInput,
    SelectInput
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
