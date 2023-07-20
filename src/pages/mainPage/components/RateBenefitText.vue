<script setup>
defineProps(["text"]);
</script>

<template>
  <div class="benefit">
    <img src="@/assets/approve.svg" alt="approve" />
    <p class="benefit__text">
      {{ text }}
    </p>
  </div>
</template>

<style scoped lang="scss">
.benefit {
  display: flex;
  margin: 16px 0;
  align-items: start;
}
</style>
