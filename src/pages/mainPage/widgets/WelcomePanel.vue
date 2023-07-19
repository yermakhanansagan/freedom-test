<script setup>
import BorderedTextLabel from '../../../components/BorderedTextLabel.vue'
import BaseButton from '../../../components/BaseButton.vue'
</script>

<template>
    <div class="welcome-panel">
        <div class="welcome-panel__left">
            <BorderedTextLabel>Онлайн-курс</BorderedTextLabel>
            <h1 class="welcome-panel__title__text">
                «Технический анализ» офлайн-курс г. Алматы
            </h1>
            <p class="welcome-panel__subtitle__text">
                 Данный курс поможет вам открыть новые возможности совершения прибыльных сделок на фондовом рынке из любой точки мира
            </p>
            <div class="welcome-panel__buttons">
                <BaseButton>Записаться на курс</BaseButton>
                <BaseButton class="welcome-panel__buttons customed-button">
                    Подобрать мне курс 
                    <img src="@/assets/right-arrow.svg" alt="arrow">
                </BaseButton>
            </div>
        </div>
        <div class="welcome-panel__right">
            <img class="welcome-panel__right__image" src="@/assets/hero-item-image-35.svg" alt="hero-image">
        </div>
    </div>
</template>

<style scoped lang="scss">
$background-bg-primary: #F5F5F7;
$brand-additional: #00E183;
.welcome-panel{
    display: flex;
    background: $background-bg-primary;
    position: relative;
    top: 0;
    width: 100vw;
    margin: 0;
    justify-content: space-between;
}

.welcome-panel__left {
    padding: 80px 64px;
    display: flex;
    flex-direction: column;
    flex: 1;
}

.welcome-panel__subtitle__text {
    padding-top: 24px;
}
.welcome-panel__buttons {
    margin: 0;
    padding: 0;
    display: flex;
    align-items: center;
    padding-top: 44px;
}
.customed-button {
    display: flex;
    margin-left: 32px;
    background: none;
    color: $brand-additional;
    align-items: center;
    padding:  16px 0;
    img {
        padding: 0;
        margin: 0;
    }
}
.welcome-panel__right {
    display: flex;
    flex: 1;
    align-items: center;
    justify-content: center;
}
</style>