<template>
    <div>
      <h2 v-if="umur >= 18">{{ pesanSelamat }}</h2>
      <p v-else>Maaf, kamu belum cukup umur.</p>
      <button @click="greet">Sapa Bro!</button>
    </div>
  </template>

<script>
export default {
  name: 'MyComponent', 
  props: ['nama','umur'],
  data() {
    return {
      pesan: 'Halo, ' + this.nama + '!'
    };
  },
  methods: {
    greet() {
      console.log('halo' +''+this.nama);
    }
  },
  computed: {
    pesanSelamat() {
      return 'Selamat datang, ' + this.nama + '!';
    }
  },
  watch: {
    umur(newUmur, oldUmur) {
      console.log('Umur berubah dari', oldUmur, 'menjadi', newUmur)
    }
  }
}

</script>
