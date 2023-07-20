<script setup>
defineEmits(["click"]);
</script>

<template>
  <button class="base-button" @click="$emit('click')">
    <slot />
  </button>
</template>

<style scoped lang="scss">
$brand-additional: #00e183;
.base-button {
  width: 100%;
  border-radius: 12px;
  background: $brand-additional;
  display: flex;
  padding: 16px 32px;
  justify-content: center;
  align-items: center;
  color: white;
  font-size: 18px;
  border: none;
  height: fit-content;
  cursor: pointer;
}
.base-button:hover {
  opacity: 0.5;
}
</style>
