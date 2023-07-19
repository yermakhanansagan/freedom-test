<script setup>
import InfoBlock from "@/pages/mainPage/components/InfoBlock.vue";
import BenefitCard from "@/pages/mainPage/components/BenefitCard.vue";

const benefits = [
  {
    title: "Знания для преумножения капитала",
    description:
      "Знания — приносящие доход, лучшее описание курсов от Freedom Academy. Мы приоткроем занавес в мир трейдинга и покажем, как на этом можно приумножить своё благосостояние. После обучения вы сможете зарабатывать на внутридневных и среднесрочных сделках из любой точки мира, имея лишь доступ в интернет.",
  },
  { title: "Сертификат", description: "В последний день занятий мы организуем фотосессию с выпускниками и проведём вручение сертификатов." },
  {
    title: "Лекционный материал",
    description:
      "Вам будут доступны лекционные материалы по программе курса, а также домашние задания для проверки и закрепления пройденного материала. Вы получите персональные комментарии от наших экспертов по выполненным заданиям.",
  },
];
</script>

<template>
  <InfoBlock :title="'Что вы получите'">
    <div class="benefits">
      <BenefitCard v-for="(benefit, index) in benefits" :key="index" :number="index + 1" :title="benefit.title" :description="benefit.description" />
    </div>
  </InfoBlock>
</template>

<style scoped lang="scss">
.benefits {
  display: flex;
}
</style>
