<script setup>
import ProductItem from '@/components/ProductItem.vue';
import pl from '@/Data/products.json';
const productList = pl;
</script>


<template>
    <section class="product section container" id="products">
        <h2 class="section__title-center">
            Check out our <br> products
        </h2>

        <p class="product__description">
            Here are some selected plants from our showroom, all are in excellent
            shape and has a long life span. Buy and enjoy best quality.
        </p>

        <div class="product__container grid">           
            <ProductItem v-for="prod in productList.products" :product="prod" :key="prod.productId" />
        </div>
    </section>
</template>