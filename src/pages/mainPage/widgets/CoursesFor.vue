<script setup>
import FeatureCell from "../components/FeatureCell.vue";
import InfoBlock from "../components/InfoBlock.vue";

const info = [
  { imgName: "icon1.svg", title: "Начинающим", description: "Тем, кто только начинает знакомство с миром трейдинга и желает освоить новые навыки и начать зарабатывать на бирже." },
  {
    imgName: "icon2.svg",
    title: "Инвесторам и трейдерам",
    description:
      "Тем, кто уже инвестирует, но хочет открыть новый подход в управлении своих финансов, увидеть торговые ошибки, скорректировать стратегию и приумножить благосостояние.",
  },
  {
    imgName: "icon3.svg",
    title: "Фрилансерам",
    description:
      "Тем, кто не привязан к работе, но обладает свободным временем, желанием развиваться и получать уникальные возможности для заработка на фондовом рынке. Хотите освоить высокодоходный навык находясь в любой точке мира, подстроить стратегию под свои ожидания по доходу и занятости? Всё это возможно с Freedom Academy.",
  },
  {
    imgName: "icon4.svg",
    title: "Штатным сотрудникам и самозанятым",
    description:
      "Тем, кто хочет найти дополнительный источник дохода или сделать инвестиции основным источником заработка. Мы научим подстраивать торговую стратегию под ваши цели и финансовые планы.",
  },
];
</script>

<template>
  <InfoBlock class="courses-for" :title="'Кому подойдёт курс'">
    <div class="courses-for__content">
      <FeatureCell v-for="(item, index) in info" :key="index" :img-name="item.imgName" :title="item.title" :description="item.description" />
    </div>
  </InfoBlock>
</template>

<style scoped lang="scss">
.courses-for__content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 24px 32px;
}
</style>
