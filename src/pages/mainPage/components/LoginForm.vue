<script setup>
import BaseInput from "@/components/BaseInput.vue";
import BaseButton from "@/components/BaseButton.vue";
import Check from "@/pages/mainPage/components/Check.vue";
import { ref } from "vue";

const value = ref("");
</script>

<template>
  <form action="post">
    <BaseInput class="margin-bottom" v-model="value" :label="'Электронная почта'" />
    <BaseInput class="margin-bottom" v-model="value" :label="'Пароль'" />
    <BaseInput class="margin-bottom" v-model="value" :label="'Применить промокод'" />
    <Check />
    <BaseButton>Перейти к оплате</BaseButton>
  </form>
</template>

<style scoped lang="scss">
.margin-bottom {
  margin-bottom: 16px;
}
</style>
