<script setup>
defineProps(["title"]);
</script>

<template>
  <div class="info-block__">
    <h1>{{ title }}</h1>
    <div>
      <slot />
    </div>
  </div>
</template>

<style scoped lang="scss">
.info-block__ {
  height: fit-content;
  width: fit-content;
  display: flex;
  flex-direction: column;
  position: relative;
}
@media screen and (max-width: 1023px) {
  .info-block__ {
    border-radius: 32px;
    background: #fff;
    width: 100%;
    padding: 16px;
  }
}
</style>
