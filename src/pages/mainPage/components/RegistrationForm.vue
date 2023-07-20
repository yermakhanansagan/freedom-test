<script setup>
import BaseInput from "@/components/BaseInput.vue";
import BaseButton from "@/components/BaseButton.vue";

import { ref } from "vue";

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

    <div class="registration-modal__form__check">
      <input id="check" type="checkbox" name="check" />
      <label for="check">Я подтверждаю, что ознакомлен и согласен с условиями оферты и даю своё согласие на сбор и обработку персональных данных</label>
    </div>
    <BaseButton>Перейти к оплате</BaseButton>
    <p class="form__registrated-text">Уже зарегестрированы? <a class="form__login-link" href="http://">Войти</a></p>
  </form>
</template>

<style scoped lang="scss">
.form__password-description {
  font-size: 14px;
  color: #919399;
}
.registration-modal__form__check {
  display: flex;
  align-items: start;
  margin: 24px 0 32px;
  input[type="checkbox"]:checked {
    border: none;
    background: none;
  }
  label {
    margin-left: 10px;
    font-size: 14px;
  }
}
.form__registrated-text {
  margin-top: 32px;
  text-align: center;
}
.form__login-link {
  text-decoration: none;
  color: #00e183;
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
