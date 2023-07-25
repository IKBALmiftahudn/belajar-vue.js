<template>
    <div>
      <h1>Aplikasi Vue.js Gue</h1>
      <MyComponent
        :nama="nama"
        :umur="umur"
        @greeted="onGreeted"
      >
        <p>Ini konten tambahan dalam slot</p>
      </MyComponent>
    </div>
  </template>
  
  <script>
  import MyComponent from './Mycomponent.vue';
  
  export default {
    components: {
      MyComponent
    },
    data() {
      return {
        nama: 'ikbal',
        umur: 25
      };
    },
    methods: {
      onGreeted() {
        console.log('Kamu udah disapa, bro!');
      }
    }
  }
  </script>