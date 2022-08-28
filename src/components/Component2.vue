<template>
  <div class="box">
   <h1>Component 2</h1>
<strong style="font-size:25px;color:red">{{sendProvide.title}}</strong>
 <button @click="executeTitle">Change Title</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
inject:["sendProvide"
],
  methods:{
   executeTitle(){
    this.sendProvide.title = "I am a new Title, I am refreshed from Component 2";
   }
  }
}
</script>


<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
