<script setup>
import { RouterLink } from 'vue-router';
const { quizQuestionLength, numberOfCorrectAnswers } = defineProps([
  'quizQuestionLength',
  'numberOfCorrectAnswers'
]);
</script>

<template>
  <div class="results">
    <p>Your results</p>
    <h1>{{ numberOfCorrectAnswers }}/{{ quizQuestionLength }}</h1>
    <RouterLink to="/" class="link">Go Back</RouterLink>
  </div>
</template>
<style scoped>
.results {
  text-align: center;
  padding: 100px 0;
}
p {
  font-size: 25px;
}

h1 {
  font-size: 80px;
}

.link {
  text-align: center;
  padding: 100px 0;
  text-decoration: none;  
}
</style>
