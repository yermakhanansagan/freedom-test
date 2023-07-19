<script setup>
import InfoPanel from './components/InfoPanel.vue';
import CoursesFor from './widgets/CoursesFor.vue';
import OverviewCourse from './widgets/OverviewCourse.vue';
import Rate from './widgets/Rate.vue';
import WelcomePanel from './widgets/WelcomePanel.vue';


</script>

<template>
    <WelcomePanel />
    <InfoPanel />
    <div class="info-block">
        <div class="info-block__blocks">
            <CoursesFor/>
            <OverviewCourse />
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

</style>