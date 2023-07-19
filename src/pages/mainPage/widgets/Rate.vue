<script setup>
import BaseButton from "@/components/BaseButton.vue";
import RateBenefitText from "@/pages/mainPage/components/RateBenefitText.vue";
import RatePrice from "@/pages/mainPage/components/RatePrice.vue";

const benefits = ["Персональный менеджер", "Электронные материалы к курсу", "Пожизненный доступ", "Сертификат", "Открытие и обслуживание счета"];
</script>
<template>
  <div class="rate-block">
    <div class="rate__content">
      <RatePrice />
      <BaseButton>Записаться</BaseButton>
      <BaseButton class="rate__gift-button">Подарить этот курс</BaseButton>
      <div class="rate__benefits">
        <h2>Ключевые преимущества</h2>
        <RateBenefitText v-for="(text, index) in benefits" :key="index" :text="text" />
      </div>
    </div>
  </div>
</template>
<style scoped lang="scss">
.rate-block {
  border-radius: 24px;
  border: 1px solid #00e183;
  background: #00e183;
  height: fit-content;
  padding-top: 32px;
  display: flex;
  flex-direction: column;
  width: 15vw;
}
.rate__content {
  background: #fff;
  border-radius: 24px;
  padding: 32px 16px;
}

.rate__gift-button {
  margin-top: 16px;
  background: #f5f5f7;
  color: #242624;
}

.rate__benefits {
  margin-top: 40px;
  h2 {
    margin: 0;
  }
}
</style>
