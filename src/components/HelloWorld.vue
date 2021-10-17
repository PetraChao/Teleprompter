<script setup lang="ts">
import { ref } from 'vue'
import  CodeMirror  from "codemirror";
console.log(CodeMirror);
import "codemirror/theme/ambiance.css";
// require("codemirror/mode/javascript/javascript");
defineProps<{ msg: string }>()

const count = ref(0)
const curCode = '';
const cmOptions = {
    value:'',
     mode:"text/javascript",
    theme: "ambiance",
    readOnly:true,
 }
</script>

<template>
  <h1>{{ msg }}</h1>
  <CodeMirror
      :value="curCode"
      :options="cmOptions"
      ref="mycode"
      class="code">
 </CodeMirror>
 ====
</template>

<style scoped>
a {
  color: #42b983;
}

label {
  margin: 0 0.5em;
  font-weight: bold;
}

code {
  background-color: #eee;
  padding: 2px 4px;
  border-radius: 4px;
  color: #304455;
}
</style>
