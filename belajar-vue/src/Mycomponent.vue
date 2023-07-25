<template>
    <div>
       <h2>Nama : {{ nama }}</h2> <br>
       <h2>Umur : {{ umur }} </h2>
    </div>
</template>

<script>
export default {
  name: 'MyComponent', // Nama komponen, bisa diubah sesuai kebutuhan
  props: ['nama','umur'], // Definisi props "nama" dan "umur"
  data() {
    return {
      message: 'Ini pesan dari komponen!'
    };
  },
  methods: {
    greet() {
      console.log('Halo, bro!');
    }    
  }
}
</script>
