<script setup>
defineProps(['title'])
</script>

<template>
    <div class="info-block">
        <h1>{{ title }}</h1>
        <div>
            <slot></slot>
        </div>
    </div>
</template>

<style scoped lang="scss">
.info-block {
    height: fit-content;
    width: fit-content;
    display: flex;
    flex-direction: column;
    position: relative;
}
</style>