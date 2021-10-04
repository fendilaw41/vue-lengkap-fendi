<template>
  <div>
  <Header @ChangeTitle="ubahText" :text="dataText"/>
  <h3>LifeCycle Hooks dan Computed Properties (Cari Data)</h3>
  <input type="text" v-model="cari" placeholder="Cari...">
  <ul>
  <li v-for="product in cariData" :key="product.id">
        {{ product.name }} - {{ product.price }}
  </li>
  </ul>
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
export default {
  name: "LifecycleHooks",
  components: { Header },
  data(){
    return {
      cari: "",
      dataText: "fendilaw",
      products: [],
    }
  },
   beforeCreate(){
    console.log("Before Create");
  },
  created(){
    this.products = [
        {id: 1, name: "Products 1", price: 3000},
        {id: 2, name: "Products 2", price: 2000},
        {id: 3, name: "Products 3", price: 6000},
        {id: 4, name: "Products 4", price: 8000},
        {id: 5, name: "Products 5", price: 9000}
    ];
  },
  beforeMount(){
    console.log("BeforeMount");
  },
  mounted(){
    console.log("Mounted");
  },
  computed: {
    cariData(){
      return this.products.filter((product) => {
        return product.name.match(this.cari);
      });
    }
  },
  methods: {
    ubahText(newText){
      this.dataText = newText;
    }
  }
 
}
</script>

<style>

</style>