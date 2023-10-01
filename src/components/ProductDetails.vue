<template>
    <div>
        <ProductItem
        v-for="product in products" 
        :key="product.id" 
        :product="product"
        />
    </div>
</template>

<script>

import ProductItem from './ProductItem.vue'
export default {
    name: 'ProductDetails',
    components: {
        ProductItem},
   data() {      
           
           return {
               products:[{
                   id:1,
                   name:'Barbi',
                   price:2000,
                   available:true
               },
               {   id:2,
                   name:'Batman',
                   price:2500,
                   available:true
               },
               {   id:3,
                   name:'Halk',
                   price:1500,
                   available:false
               },
           ],
            
           };
       },         
   
  
}

</script>



<style lang="scss" scoped>


</style>