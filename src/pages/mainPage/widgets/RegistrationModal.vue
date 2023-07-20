<script setup>
import ModalWindow from "@/components//ModalWindow.vue";
import InfoCard from "../components/InfoCard.vue";
import RegistrationForm from "@/pages/mainPage/components/RegistrationForm.vue";
import LoginForm from "../components/LoginForm.vue";

import { ref } from "vue";

defineProps(["isOpen"]);

const registration = ref(false);
</script>

<template>
  <ModalWindow>
    <div class="registration-modal">
      <div class="registration-modal__header">
        <h2 class="form__header">Заполните форму</h2>
        <p class="form__header-description">Для оформления заказа, заполните поля ниже</p>
      </div>
      <InfoCard />
      <div>
        <h2 class="form__header">Заполните форму</h2>
        <p class="form__header-description">Для оформления заказа, заполните поля ниже</p>
        <RegistrationForm v-if="registration" />
        <LoginForm v-else />
      </div>
    </div>
  </ModalWindow>
</template>

<style scoped lang="scss">
.registration-modal {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 48px;
  text-align: start;
  height: fit-content;
}
.registration-modal__header {
  display: none;
}
.form__header-description {
  margin: 8px 0 16px;
  font-size: 14px;
}
.form__header {
  margin: 0;
}

@media screen and (max-width: 1023px) {
  .registration-modal {
    display: flex;
    flex-direction: column;
  }
  .registration-modal__header {
    display: flex;
  }
  .form__header {
    display: none;
  }
  .form__header-description {
    display: none;
  }
}
</style>
