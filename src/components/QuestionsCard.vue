<script setup>
    import { toRefs } from "vue";

    const props = defineProps({
        qData: Object,
    });

    const { qData } = toRefs(props);
    let showAnswer = false;

    function toggleStyle() {
        const element = document.getElementsByClassName('questions__item')[qData.value.questionId-1];
        const question = document.getElementsByClassName('questions__header')[qData.value.questionId-1];
        const answerElement = document.getElementsByClassName('questions__content')[qData.value.questionId-1];
        if (!showAnswer){
            element.classList.add('accordion-open');
            answerElement.style.height = answerElement.scrollHeight + 'px';
            showAnswer = true;
        }
        else {
            element.classList.remove('accordion-open');
            answerElement.removeAttribute('style');
            showAnswer = false;
        }
    }
</script>

<template>
    <div class="questions__group" @click="toggleStyle">
        <div class="questions__item">
            <header class="questions__header">
                <i class="ri-add-line questions__icon"></i>
                <h3 class="questions__item-title">
                    {{qData.question}}
                </h3>
            </header>

            <div class="questions__content">
                <p class="questions__description">
                    {{qData.answer}}
                </p>
            </div>
        </div>
    </div>
</template>
