<script setup>
defineProps(["imgName", "title", "description"]);
</script>

<template>
  <div class="feature-cell">
    <img class="feature-cell__icon" :src="'/src/assets/' + imgName" :alt="imgName" />
    <div class="feature-cell__texts">
      <h3 class="feature-cell__title">
        {{ title }}
      </h3>
      <p class="feature-cell__description">
        {{ description }}
      </p>
    </div>
  </div>
</template>

<style scoped lang="scss">
.feature-cell {
  width: 100%;
  display: flex;
  align-items: start;
}
.feature-cell__icon {
  width: 64px;
  height: 64px;
  background: #f5f5f7;
  border-radius: 8px;
}
.feature-cell__texts {
  margin-left: 24px;
}
.feature-cell__title {
  padding: 0;
  margin: 0;
}

@media screen and (max-width: 1023px) {
  .feature-cell {
    width: 240px;
    flex-direction: column;
  }
  .feature-cell__texts {
    margin-left: 0;
    margin-top: 16px;
  }
}
</style>
