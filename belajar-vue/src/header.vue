<template>
    <div>
       <center> <h2>Judul : {{ text }}</h2> </center>   
    </div>
</template>

<script>
    export default{
        name: 'Header', // Nama komponen, bisa diubah sesuai kebutuhan
  props: ['text'],
    };
</script> 