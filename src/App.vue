<template>
  <div class="hello">
    <h1>Inject and Provide consepts in VUEJS Components</h1>
    <Component1 />
    <Component2 />
  </div>
</template>

<script>
import Component1 from "./components/Component1.vue";
import Component2 from "./components/Component2.vue";

export default {
  name: "App",
  components: {
    Component1,
    Component2,
  },
  provide() {
    return {
      sendProvide: this.sendProvide,
    };
  },

  data() {
    return {
      sendProvide: {
        title: "I am a title",
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
.box {
  width: 400px;
  border: 3px solid red;
  margin: auto auto;
  padding: 15px;
  margin-top: 20px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: center;
}
button{

  width: 100px;
  margin: auto;
  padding: 10px;
  
}
</style>
