<template>
  <div>
<Header text></Header>
    <!-- <h1>Aplikasi Vue.js Gue</h1> -->
    <!-- <my-component nama="John" umur="25"></my-component> -->
    <!-- <NewComponent></NewComponent> -->
    <!-- <Footercomponent></Footercomponent> -->
    <Latihancomponent nama="ikbal" umur="90" ></Latihancomponent>
    <Latihan2component></Latihan2component>
    <Watchercomponent nama="watcher" umur="110"></Watchercomponent>
    <Eventcomponent></Eventcomponent>
  </div>
</template>

<script setup>
import Watchercomponent from './watchercomponent.vue';

import Latihancomponent from './latihancomponent.vue'; 
// import NewComponent from './Newcomponent.vue';
// import Footercomponent from './footercomponent.vue';
// import Header from './header.vue';
import Latihan2component from './latihan2component.vue';
import Eventcomponent from './eventcomponent.vue';



</script>