<script setup>
import { ref } from 'vue'
 
//no rawHtml
const msg ="<h1>Hello World</h1>"
//rawHtml n(menggunakan html yang ada dalam variable )
const rawHtml = " <h1> <font color = 'blue'> Hello World </font> </h1>"
// v-bind (menggunakan atribut html ke vue.js)
const link = "https://github.com/"
//aritmatika
const number= prompt("")
</script>

<template>
  <div id="app">
    <span>{{ msg }}</span><br>
    <p><span v-html="rawHtml"></span></p><br>
    <a :href="link">Github</a><br>
    <p>{{ parseInt(number) }}</p>
    <p>{{ number ? 'TRUE : 1' : 'FALSE : 0' }}</p>
    <br>
    <button :disabled="isButtonDisabled">Button</button>
  
  </div>
</template>