<script setup>
import InfoBlock from '../components/InfoBlock.vue'
import BaseButton from '../../../components/BaseButton.vue'
</script>

<template>
    <InfoBlock class="overview" :title="'Обзор курса'">
    <p class="overview__description">
        Мы специально подготовили тизер курса чтобы вы смогли больше ознакомиться с тем что вас ждет. Курс поможет Вам сделать первые шаги в мире инвестиций и открыть новые возможности для сохранения и приумножения капитала.
    </p>
    <div class="overview__vider-container">
        <iframe src="https://www.youtube.com/embed/tgbNymZ7vqY"></iframe>
        <BaseButton class="overview-button">Смотреть сейчас <img src="../../../assets/play-icon.svg" alt="play"></BaseButton>
    </div>
    </InfoBlock>
</template>

<style scoped lang="scss">
.overview__description {
    width: 40vw;
    text-align: justify;
}
.overview__vider-container {
    margin-top: 48px;
    position: relative;
    iframe{
        width: 60vw;
        height: 480px;
        border-radius: 8px;
        border: none;
    }
}
.overview-button {
    position: absolute;
    border-radius: 20px;
    background: #FFFFFF;
    bottom: 24px;
    left: 24px;
    z-index: 2;
    color: #242624;
    width: fit-content;
    img {
        margin-left: 12px;
    }
}
</style>