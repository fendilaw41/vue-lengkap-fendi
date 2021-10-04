<template>
 <div v-if="products.length">
    <h2>Berikut adalah Two way Binding dan Looping</h2>
    <input type="text" v-model="nama" />
    {{ nama }}
    <h2>Berikut adalah Looping</h2>
    <ul>
        <li v-for="product in products" :key="product.id">
            {{ product.name }}
            {{ product.price }}
        </li>
    </ul>
 </div>
   <div v-else>
  <h3>Data Kosong</h3>
  </div>
</template>

<script>
export default {
    name: "Two-Way",

    data(){
        return {
            nama: "",
            products: [
                { id: 1, name: "Product 1", price: 4000 },
                { id: 2, name: "Product 2", price: 6000 },
                { id: 3, name: "Product 3", price: 2000 },
                { id: 4, name: "Product 4", price: 1000 },
                { id: 5, name: "Product 5", price: 7000 }
            ]
        }
    }
}
</script>

<style>

</style>