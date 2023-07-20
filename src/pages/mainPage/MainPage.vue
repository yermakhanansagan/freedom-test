<script setup>
import InfoPanel from "./components/InfoPanel.vue";
import Benefits from "./widgets/Benefits.vue";
import CoursesFor from "./widgets/CoursesFor.vue";
import OverviewCourse from "./widgets/OverviewCourse.vue";
import Rate from "./widgets/Rate.vue";
import WelcomePanel from "./widgets/WelcomePanel.vue";
</script>

<template>
  <WelcomePanel />
  <InfoPanel />
  <div class="info-block">
    <div class="info-block__blocks">
      <Benefits class="margin-bottom" />
      <CoursesFor class="margin-bottom" />
      <OverviewCourse class="margin-bottom" />
    </div>
    <div class="rate">
      <Rate />
    </div>
  </div>
</template>

<style scoped lang="scss">
.info-block {
  padding: 0 40px;
  position: relative;
  display: flex;
}
.info-block__blocks {
  width: 70vw;
}

.rate {
  width: 100%;
  display: flex;
  justify-content: center;
}

@media screen and (max-width: 1023px) {
  .info-block {
    background: #f5f5f7;
    padding: 8px;
    flex-direction: column;
  }

  .info-block__blocks {
    width: 100%;
  }
  .margin-bottom {
    margin-bottom: 16px;
  }
}
</style>
