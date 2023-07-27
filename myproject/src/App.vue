<template>
  <div>
    <navbarComponent></navbarComponent>
    <headerComponent></headerComponent>
    <contentComponent></contentComponent>
    <br>
    <br>
    <ContactComponent></ContactComponent>
    <br>
    <br>
    <footerComponent></footerComponent>
  </div>

  </template>

  <script setup>
import navbarComponent from './components/navbarComponent.vue';
import headerComponent from './components/headerComponent.vue'
import contentComponent from './components/contentComponent.vue'
import footerComponent from './components/footerComponent.vue'
import ContactComponent from './components/contactComponent.vue';
</script>