<template>
     <div>
        <div class="product">
        <h2> Название товара: <span class="product__name">{{ product.name }}</span></h2>
        <h3>Цена в рублях: {{ product.price }} </h3>
        <h3>Цена в долларах: {{ formattedPrice }}$</h3>
        <h3 v-if="product.available"><span class="product__available">Available</span></h3>
        <h3 v-else><span class="product__out">Out of stock</span></h3>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ProductItem',
    props: ['product'],
    data(){
    return {
          }},    

    computed:{
        formattedPrice() {
            return this.product.price/100
    }
    }
};
</script>

<style lang="scss" scoped>
.product{
    margin: 50px auto;
    display: flex;
    flex-direction: column;
    text-align: start;
    &__name{
        color: #8A2BE2;
    }
    &__available{
        color: chartreuse;
    }
    &__out{
        color: brown;
    }
}
</style>