<script setup>
import BaseInput from "@/components/BaseInput.vue";
import BaseButton from "@/components/BaseButton.vue";

import { ref } from "vue";
import Check from "./Check.vue";

const name = ref("");
const email = ref("");
const phone = ref("");
const password = ref("");
const code = ref("");
</script>

<template>
  <form action="post">
    <BaseInput v-model="name" :label="'Фамилия и имя'" />
    <div class="spaced margin-top">
      <BaseInput v-model="email" :label="'Электронная почта'" type="email" />
      <BaseInput v-model="phone" :label="'Номер телефона'" type="phone" />
    </div>
    <BaseInput v-model="password" class="margin-top" :label="'Придумайте пароль'" type="password" />
    <p class="form__password-description">6 — более символов, минимум 1 цифра, латинские буквы</p>
    <BaseInput v-model="code" class="margin-top" :label="'Применить промокод'" />
    <Check />
    <BaseButton>Перейти к оплате</BaseButton>
  </form>
</template>

<style scoped lang="scss">
.form__password-description {
  font-size: 14px;
  color: #919399;
}
.spaced {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 16px;
}
.margin-top {
  margin-top: 16px;
}

@media screen and (max-width: 1023px) {
  .spaced {
    display: flex;
    flex-direction: column;
  }
}
</style>
