<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h1>{{ count }}</h1>
     <input type="button" @click="onAdd" value="子点击一下" />
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'HelloWorld',
  props: {
    msg: String,
  }, 
 
  setup(){
    const count  = ref(0);
    function onAdd(){
        count.value++;
      }
    return {
        count,
        onAdd
    }
  }
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
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
