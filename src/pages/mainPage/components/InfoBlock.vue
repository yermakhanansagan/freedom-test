<script setup>
defineProps(['title'])
</script>

<template>
    <div class="info-block">
        <h1>{{ title }}</h1>
        <slot></slot>
    </div>
</template>

<style scoped lang="scss">
.info-block {
    height: fit-content;
    width: fit-content;
}
</style>