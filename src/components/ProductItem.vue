<template>
    <article class="product__card">
        <div class="product__circle"></div>

        <img :src="product.srcImage" alt="" class="product__img">

        <h3 class="product__title">{{product.productName}}</h3>
        <span class="product__price">&#8377;{{product.productPrice}}</span>

        <button class="button--flex product__button">
            <i class="ri-shopping-bag-line"></i>
        </button>
    </article>
</template>

<script setup>
    const props = defineProps({
        product: Object,
    });
</script>