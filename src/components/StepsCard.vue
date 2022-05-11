<template>
    <div class="steps__card">
        <div class="steps__card-number"> {{cardDetails.stepNo}} </div>
        <h3 class="steps__card-title"> {{cardDetails.stepTitle}} </h3>
        <p class="steps__card-description">
            {{cardDetails.stepDescription}}
        </p>
    </div>
</template>

<script setup>
const props = defineProps({
    cardDetails:Object,
})
</script>
