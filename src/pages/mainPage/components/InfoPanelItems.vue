<script setup>
defineProps(["title", "description"]);
</script>

<template>
  <div class="info-panel__item">
    <div class="info-panel__items-title">
      {{ title }}
    </div>
    <p class="info-panel__items-description">
      {{ description }}
    </p>
  </div>
</template>

<style scoped lang="scss">
.info-panel__item {
  text-align: center;
  flex: 1;
}
.info-panel__items-title {
  font-size: 24px;
  font-style: normal;
  font-weight: 700;
}
.info-panel__items-description {
}
</style>
