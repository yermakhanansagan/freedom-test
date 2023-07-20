<script setup>
import SlideFadeTransition from "@/transitions/SlideFadeTransition.vue";

defineEmits(["close"]);
</script>

<template>
  <SlideFadeTransition>
    <div class="modal-overlay">
      <div class="modal">
        <img class="modal-close" src="@/assets/close.svg" alt="close" @click="$emit('close')" />
        <slot />
      </div>
    </div>
  </SlideFadeTransition>
</template>

<style scoped lang="scss">
.modal-overlay {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  display: flex;
  justify-content: center;
  background-color: #000000da;
  z-index: 999;
}

.modal {
  margin-top: 5%;
  text-align: center;
  background: #fff;
  padding: 2vw;
  border-radius: 24px;
  min-height: 60vh;
  height: fit-content;
  width: 50vw;
}
.modal-close {
  position: fixed;
  top: 20px;
  right: 20px;
  cursor: pointer;
}

@media screen and (max-width: 1023px) {
  .modal {
    height: 100%;
    overflow-y: auto;
    padding-bottom: 10%;
  }
}
</style>
