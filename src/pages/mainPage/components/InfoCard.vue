<script setup>
import BorderedTextLabel from "@/components/BorderedTextLabel.vue";
import RateBenefits from "@/pages/mainPage/components/RateBenefits.vue";

const benefits = ["Персональный менеджер", "Электронные материалы к курсу", "Пожизненный доступ", "Сертификат", "Открытие и обслуживание счета"];
</script>

<template>
  <div class="info">
    <div class="info__header spaced">
      <BorderedTextLabel>Вебинар</BorderedTextLabel>
      <p class="info__header-lang">Рус</p>
    </div>
    <div class="info-name">
      <div class="info-name__text">
        <h3>«Технический анализ Pro» - авторский онлайн курс Елены Беляевой</h3>
        <p>24–31 января, 19:00–21:00</p>
        <p>Спикер: Елена Беляева</p>
      </div>
      <img class="info-name__logo" src="@/assets/logo.svg" alt="logo" />
    </div>
    <div class="divider" />
    <div class="info-price">
      <h3>Стоимость курса</h3>
      <div class="info-prices">
        <div class="info-price__price">
          <h3>30 000</h3>
          <p>₸/мес</p>
        </div>
        <div class="info-price__price changed">
          <h3>60 000 ₸/мес</h3>
        </div>
      </div>
      <RateBenefits class="info-benefits" :benefits="benefits" />
    </div>
  </div>
</template>

<style scoped lang="scss">
.info {
  display: flex;
  flex-direction: column;
  padding: 1.5vw;
  border-radius: 24px;
  background: #f5f5f7;
}
.info__header-lang {
  color: #000000;
  font-size: 14px;
}
.info-name {
  display: flex;
  margin-top: 16px;
}
.info-name__text {
  display: flex;
  flex-direction: column;
  flex: 2;
  padding-right: 15px;
}
.info-name__logo {
  flex: 1;
}
.info-prices {
  display: flex;
}
.info-price__price {
  display: flex;
  align-items: center;
}
.info-benefits {
  margin: 0;
  p {
    font-size: 14px;
  }
}
.divider {
  height: 1px;
  background: #dee0e3;
  margin: 16px 0;
}
.spaced {
  display: flex;
  justify-content: space-between;
}
.changed {
  margin-left: 8px;
  text-decoration-line: line-through;
  color: #919399;
}
h3 {
  margin: 0;
}
h2 {
  margin: 0;
  font-size: 1.17em;
}

@media screen and (max-width: 1023px) {
  .info-name__logo {
    display: none;
  }
}
</style>
