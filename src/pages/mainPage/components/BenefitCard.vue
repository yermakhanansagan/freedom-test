<script setup>
defineProps(["number", "title", "description"]);
</script>

<template>
  <div class="card">
    <div class="card__number">
      {{ number }}
    </div>
    <h3 class="card__title">{{ title }}</h3>
    <p class="card__description">{{ description }}</p>
  </div>
</template>

<style scoped>
.card {
  width: 320px;
  height: 100%;
  border-radius: 32px;
  background: #f5f5f7;
  padding: 24px;
  margin: 12px;
}
.card__number {
  border: 1px solid #00e183;
  border-radius: 50%;
  color: #00e183;
  font-size: 24px;
  font-weight: 700;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 48px;
  width: 48px;
}
.card__title {
  margin-top: 32px;
}

.card__description {
  margin-top: 16px;
}
</style>
