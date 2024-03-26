<script setup>
import DataService from "../services/dataservice";
import { ref, onMounted } from "vue";
  const products = ref([])
  DataService.getAllProducts().then(resp => {
          
                products.value = resp.data
                
            })
            .catch(err =>{
               console.log(err);
               
            })

</script>

<template>
  <select name="" id="">
    <option v-for="product in products" value="">{{ product.manufacturer_id }}</option>
  </select>
  
</template>
