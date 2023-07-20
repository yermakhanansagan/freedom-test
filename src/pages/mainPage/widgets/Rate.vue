<script setup>
import BaseButton from "@/components/BaseButton.vue";
import RatePrice from "@/pages/mainPage/components/RatePrice.vue";
import RateBenefits from "@/pages/mainPage/components/RateBenefits.vue";

const benefits = ["Персональный менеджер", "Электронные материалы к курсу", "Пожизненный доступ", "Сертификат", "Открытие и обслуживание счета"];
</script>

<template>
  <div class="rate-block">
    <div class="rate__content">
      <RatePrice />
      <RateBenefits class="rate__benefits-small" :benefits="benefits" />
      <BaseButton>Записаться</BaseButton>
      <BaseButton class="rate__gift-button"> Подарить этот курс </BaseButton>
      <RateBenefits class="rate__benefits-big" :benefits="benefits" />
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
  z-index: 3;
}
.rate__content {
  background: #fff;
  border-radius: 24px;
  padding: 32px 16px;
}
.rate__benefits-small {
  display: none;
}
.rate__gift-button {
  margin-top: 16px;
  background: #f5f5f7;
  color: #242624;
}
@media screen and (max-width: 1023px) {
  .rate-block {
    width: 100%;
    background: #fff;
    border: none;
    padding: 0;
  }
  .rate__content {
    padding: 20px 16px;
  }
  .rate__benefits-small {
    display: block;
    margin-bottom: 16px;
  }
  .rate__benefits-big {
    display: none;
  }
}
</style>
