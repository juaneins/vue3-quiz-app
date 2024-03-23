<script setup>
import { ref } from 'vue';
import QuestionComponent from '@/components/QuestionComponent.vue';
import QuizHeaderComponent from '@/components/QuizHeaderComponent.vue';
import { useRoute } from 'vue-router';
import quizes from '@/data/quizes.json';

const route = useRoute();

const quizId = parseInt(route.params.id);

const quiz = quizes.find((q) => q.id === quizId);

const currentQuestionIndex = ref(0);
</script>
<template>
  <div>
    <QuizHeaderComponent />
    <div>
      <QuestionComponent :question="quiz.questions[currentQuestionIndex]" />
    </div>
  </div>
</template>
