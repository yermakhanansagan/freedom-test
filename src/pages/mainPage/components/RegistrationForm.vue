<script setup>
import BaseInput from "@/components/BaseInput.vue";
import BaseButton from "@/components/BaseButton.vue";
import Check from "./Check.vue";

import { ref } from "vue";
import { object, string } from "yup";
import { useForm } from "vee-validate";

const reqValue = "Заполните поле";

const name = ref("");
const email = ref("");
const phone = ref("");
const password = ref("");
const code = ref("");

const isNotReadyToLogin = ref(true);

const schema = object({
  name: string().required(reqValue),
  email: string().required(reqValue).email("Не валидный email"),
  phone: string().required(reqValue),
  password: string()
    .required(reqValue)
    .min(6, "6 — более символов")
    .matches(/[a-zA-Z0-9]/, "Минимум 1 цифра, латинские буквы"),
});

const check = (value) => (isNotReadyToLogin.value = value);

const { handleSubmit } = useForm({ validationSchema: schema });

const login = handleSubmit(
  () => {
    console.log("success");
  },
  () => {
    console.log("error");
  }
);
</script>

<template>
  <form action="post" @submit.prevent="login">
    <BaseInput v-model="name" :label="'Фамилия и имя'" name="name" />
    <div class="spaced margin-top">
      <BaseInput v-model="email" :label="'Электронная почта'" type="email" name="email" />
      <BaseInput v-model="phone" :label="'Номер телефона'" type="phone" name="phone" />
    </div>
    <BaseInput v-model="password" class="margin-top" :label="'Придумайте пароль'" type="password" name="password" />
    <p class="form__password-description">6 — более символов, минимум 1 цифра, латинские буквы</p>
    <BaseInput v-model="code" class="margin-top" :label="'Применить промокод'" name="code" />
    <Check @check="check" />
    <BaseButton :disabled="isNotReadyToLogin">Перейти к оплате</BaseButton>
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
