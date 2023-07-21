<template>
  <div>
  <h2>Formulir</h2>
  <form @submit.prevent="submitForm">
      <label for="">Nama</label>
      <input  type="text" name="nama" v-model="siswa.nama">
      <br>
      <label for="">Kelas</label>
      <input  type="text" name="kelas" v-model="siswa.kelas">
      <br>
      <label for="">Alamat</label>
      <input type="textarea" name="alamat" v-model="siswa.alamat">
      <br>
      <label for="">Nilai Matematika</label>
      <input type="text" name="mtk" v-model="siswa.mtk">
      <br>
      <label for="">NIlai B.Indonesia</label>
      <input type="text" name="indo" v-model="siswa.indo">
      <br>
      <label for="">Nilai IPA</label>
      <input type="text" name="ipa" v-model="siswa.ipa">
      <br>
      <button type="submit">Simpan</button>
    </form>
    <div v-if="showResult">
      nama : {{ name }} <br>
      kelas : {{ kelas }} <br>
      alamat : {{ alamat }} <br>
      Nilai Matematika : {{ mtk }} <br>
      Nilai Indonesia : {{ indo }} <br>
      Nilai IPA : {{ ipa }} <br>
      Total : {{ total }} <br>
      Keterangan : {{ keterangan }}
    </div>
  </div>
</template>

<script>
import { ref, toDisplayString } from 'vue';

export default {
  name  : 'Mycomponent',
  data() {
    return {
      siswa: {
        nama: '',
        kelas: '',
        alamat: '',
        mtk:'',
        indo:'',
        ipa:'',
      },
      
      showResult: ref(false),
      name: ref(''),
      kelas: ref(''),
      alamat: ref(''),
      mtk: ref(''),
      indo: ref(''),
      ipa: ref(''),
      total : 0 ,
      keterangan : ref('')
    };
  },
 
 
  methods: {
    submitForm() {
      this.name = this.siswa.nama;
      this.kelas = this.siswa.kelas;
      this.alamat = this.siswa.alamat;
      this.mtk = this.siswa.mtk;
      this.indo = this.siswa.indo;
      this.ipa = this.siswa.ipa;
      this.total = parseInt(this.mtk) + parseInt(this.indo) + parseInt(this.ipa);
      if (this.total >240){
        this.keterangan ="Lulus"
      }else{
        this.keterangan ="Tidak Lulus"
      }
      this.showResult = true;
    },
  },
};
</script>