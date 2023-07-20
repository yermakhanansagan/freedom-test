<script setup>
import { computed } from "vue";

const props = defineProps(["modelValue", "label", "type"]);
defineEmits(["update:modelValue"]);

const isValueExist = computed(() => props.modelValue.length);
</script>

<template>
  <div class="base-input__container">
    <input
      id="input"
      class="base-input"
      :class="{ 'with-value': isValueExist }"
      :type="type"
      :value="modelValue"
      :placeholder="label"
      @input="$emit('update:modelValue', (modelValue = $event.target.value))"
    />
    <label v-if="isValueExist" class="base-input__label" for="input">{{ label }}</label>
  </div>
</template>

<style scoped lang="scss">
.base-input__container {
  position: relative;
}
.base-input {
  width: 100%;
  outline: none;
  border: none;
  padding: 16px 0 16px 20px;
  border-radius: 12px;
  border: 1px solid var(--divider-divider-primary, #dee0e3);
  background: var(--grey-0, #fff);
  box-sizing: border-box;
}

.base-input__label {
  position: absolute;
  top: 6px;
  left: 20px;
  font-size: 12px;
  color: #919399;
}

.with-value {
  padding: 22px 0 10px 20px;
}
</style>
