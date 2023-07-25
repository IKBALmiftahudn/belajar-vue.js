<template>
    <div>
   <input type="text" v-model="cari" placeholder="Cari Data">
   <ul>
    <li v-for="item in cariData" :key="item.id">
    {{ item.title }} - {{ item.price }}</li>
   </ul>
   <p v-if="cariData.length ===0">Tidak Ada Pencarian</p>
    </div>
</template>

<script>
export default{
    data(){
        return{
            cari: '',
            product :[]
        };
    },
    created(){
        this.product = [
            {id:1 , title:"Baju Anak" , price: 25000},
            {id:2 , title:"Susu Anak" , price: 25000},
            {id:3 , title:"Topi" , price: 25000},
            {id:4 , title:"Celana Anak" , price: 25000},
            {id:5 , title:"Baju DEWASA" , price: 25000}
    ]
    },
  computed :{
    cariData(){
        return this.product.filter((item) => {
            return item.title.match(this.cari);
        })
    }
  }
}
</script>