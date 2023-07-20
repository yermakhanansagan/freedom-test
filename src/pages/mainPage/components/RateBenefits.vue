<script setup>
import RateBenefitText from "@/pages/mainPage/components/RateBenefitText.vue";
import { ref } from "vue";

defineProps(["benefits"]);

const showBenefits = ref(false);
</script>
<template>
  <div class="rate__benefits">
    <h2>
      Ключевые преимущества
      <button class="rate__header-arrow">
        <img src="@/assets/arrow-bottom.svg" alt="arrow" @click="showBenefits = !showBenefits" />
      </button>
    </h2>
    <div class="hide" :class="{ show: showBenefits }">
      <RateBenefitText v-for="(text, index) in benefits" :key="index" :text="text" />
    </div>
  </div>
</template>

<style scoped lang="scss">
.rate__benefits {
  margin-top: 40px;
  h2 {
    margin: 0;
    display: flex;
    align-items: center;
  }
}
.rate__header-arrow {
  display: none;
  margin-left: 12px;
}
@media screen and (max-width: 1023px) {
  .rate__benefits {
    h2 {
      font-size: 1.17em;
    }
  }
  .rate__header-arrow {
    display: flex;
    background: none;
    border: none;
    cursor: pointer;
  }
  .hide {
    display: none;
  }
  .show {
    display: flex;
    flex-direction: column;
  }
}
</style>
