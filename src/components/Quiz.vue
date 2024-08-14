<template>
  <div class="quiz__container">
    <div class="question__container">
      <h1 class="question">Де правильна відповідь?</h1>
    </div>
    <div class="answers__container">
      <div class="answer__container">
        <p>Не правильна відповідь</p>
      </div>
      <div class="answer__container">
        <p>Не правильна відповідь</p>
      </div>
      <div class="answer__container">
        <p>Правильна відповідь</p>
      </div>
      <div class="answer__container">
        <p>Не правильна відповідь</p>
      </div>
    </div>
    <div class="steps__container">
      <p>4/5</p>
      <img src="/next-question.svg" alt="" />
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const questions = ref([
  {
    id: 1,
    question: "Скільки стовпчиків в таблиці?",
    answer: "4",
  }
])

</script>












<style lang="scss">
@import "../assets/styles/_vars.scss";
.quiz__container {
  margin-top: 69px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.question__container {
  color: $text-color;
}

.answers__container {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  gap: 20px;

  @media screen and (max-width: 768px) {
    flex-direction: column;
    gap: 10px;
    width: 100%;
  }
}

.answer__container {
  display: flex;
  height: 300px;
  padding: 30px;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 24px;
  border-radius: 8px;
  border: 3px solid $border-color;
  background: var(--Colors-Base-Grey-4, #1d2330);
  margin-top: 30px;

  &:hover {
    cursor: pointer;
    border-color: rgb(121, 25, 255);
    transition: all 0.3s linear;
  }
  p {
    color: $text-color;
    font-size: 24px;
    text-align: center;
  }
}

.steps__container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-top: 30px;
  color: $text-color;
  width: 100%;
  font-size: 24px;
}
</style>
