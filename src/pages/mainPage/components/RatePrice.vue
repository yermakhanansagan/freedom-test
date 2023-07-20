<script setup></script>

<template>
  <div class="rate__price">
    <p class="rate__old-price">60 000 ₸ / мес</p>
    <div class="rate__new-price">
      <h1>30 000</h1>
      <p>₸/мес</p>
    </div>
    <div class="rate__deadline">цена актуальна до 01.12.2022</div>
  </div>
</template>

<style scoped lang="scss">
.rate__old-price {
  font-size: 14px;
}
.rate__new-price {
  margin: 16px 0;
  display: flex;
  h1 {
    margin: 0;
  }
}
.rate__deadline {
  font-size: 14px;
  color: #919399;
  margin-bottom: 32px;
}

@media screen and (max-width: 1023px) {
  .rate__price {
    position: relative;
  }
  .rate__deadline {
    position: absolute;
    margin: 0;
    top: 0;
    right: 0;
  }
}
</style>
