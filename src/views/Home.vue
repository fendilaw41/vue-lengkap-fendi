<template>
  <div class="home" >
  <Header @ChangeTitle="ubahText" :text="dataText" />
    <h3>Berikut Adalah Data dan Methods</h3>
    <h2>{{ nama }}</h2>
    <button @click="changeName">Ganti Nama</button>
  </div>

</template>

<script>
import Header from '@/components/Header.vue'
export default {
  name: 'Home',
  components: {
    Header
  },
  data(){
    return {
      nama: "fendi",
      dataText: "ini adalah text dari data Home.vue"
    }
  },
  
  
  methods: {
    changeName(){
      this.nama = "Law";
    },
    ubahText(newText){
      this.dataText = newText;
    }
  }
 
}
</script>
