<script setup>
import InfoPanel from './components/InfoPanel.vue';
import CoursesFor from './widgets/CoursesFor.vue';
import OverviewCourse from './widgets/OverviewCourse.vue';
import WelcomePanel from './widgets/WelcomePanel.vue';


</script>

<template>
    <WelcomePanel />
    <InfoPanel />
    <div class="info-blocks">
        <CoursesFor />
        <OverviewCourse />
    </div>
</template>

<style scoped lang="scss">
.info-blocks {
    padding: 0 40px;
}
</style>