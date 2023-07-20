<script setup>
import InfoPanelItems from "../components/InfoPanelItems.vue";

const panelText = [
  { title: "11 марта 2021", description: "Дата проведения" },
  { title: "19:00 мск", description: "Время проведения" },
  { title: "Алматы", description: "Место проведения" },
  { title: "5", description: "Модулей" },
];
</script>

<template>
  <div class="info-panel">
    <InfoPanelItems v-for="(item, index) in panelText" :key="index" :title="item.title" :description="item.description" />
  </div>
</template>

<style scoped lang="scss">
.info-panel {
  display: flex;
  margin: 48px;
}
@media screen and (max-width: 1023px) {
  .info-panel {
    width: 100%;
    flex-direction: column;
    align-items: start;
    text-align: start;
    background: #fff;
    margin: 8px;
    padding: 0 20px;
    border-radius: 0 0 32px 32px;
  }
}
</style>
