<script setup></script>

<template>
  <div class="bordered__text">
    <slot />
  </div>
</template>

<style scoped lang="scss">
.bordered__text {
  padding: 8px 12px;
  align-items: flex-start;
  border-radius: 8px;
  border: 1px solid #dee0e3;
  height: fit-content;
  width: fit-content;
}
</style>
