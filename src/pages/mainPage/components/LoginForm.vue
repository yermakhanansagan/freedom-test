<script setup>
import BaseInput from "@/components/BaseInput.vue";
import BaseButton from "@/components/BaseButton.vue";
import Check from "@/pages/mainPage/components/Check.vue";
import { ref } from "vue";
import { object, string } from "yup";
import { useForm } from "vee-validate";

const reqValue = "Заполните поле";

const email = ref("");
const password = ref("");
const code = ref("");

const isNotReadyToLogin = ref(true);

const check = (value) => (isNotReadyToLogin.value = value);

const schema = object({
  email: string().required(reqValue).email("Не валидный email"),
  password: string()
    .required(reqValue)
    .min(6, "6 — более символов")
    .matches(/[a-zA-Z0-9]/, "Минимум 1 цифра, латинские буквы"),
});

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
    <BaseInput class="margin-bottom" v-model="email" :label="'Электронная почта'" name="email" />
    <BaseInput class="margin-bottom" v-model="password" :label="'Пароль'" name="password" />
    <BaseInput class="margin-bottom" v-model="code" :label="'Применить промокод'" name="code" />
    <Check @check="check" />
    <BaseButton :disabled="isNotReadyToLogin">Перейти к оплате</BaseButton>
  </form>
</template>

<style scoped lang="scss">
.margin-bottom {
  margin-bottom: 16px;
}
</style>
