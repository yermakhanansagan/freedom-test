<script setup></script>

<template>
  <div class="registration-modal__form__check">
    <input id="check" type="checkbox" name="check" />
    <label for="check">Я подтверждаю, что ознакомлен и согласен с условиями оферты и даю своё согласие на сбор и обработку персональных данных</label>
  </div>
</template>

<style scoped lang="scss">
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
</style>
