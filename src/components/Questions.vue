<script setup>
import QuestionsCard from '@/components/QuestionsCard.vue';
import questionsData from '@/Data/questions.json';
const questionData = questionsData;
</script>

<template>
    <section class="questions section" id="faqs">
        <h2 class="section__title-center questions__title container">
            Some common questions <br> were often asked
        </h2>

        <div class="questions__container container grid">
            <QuestionsCard v-for="qd in questionData.questions" :qData="qd" :key="qd.questionId"/>
        </div>
    </section>
</template>