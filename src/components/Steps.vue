<script setup>
import StepsCard from '@/components/StepsCard.vue';
import data from '@/Data/steps.json';
const cardDetailsList = data;
</script>


<template>
    <section class="steps section container">
        <div class="steps__bg">
            <h2 class="section__title-center steps__title">
                Steps to start your <br> plants off right
            </h2>

            <div class="steps__container grid">
                <StepsCard v-for="cardDetails in cardDetailsList.steps" :key="cardDetails.stepNo" :cardDetails="cardDetails" />
            </div>
        </div>
    </section>
</template>