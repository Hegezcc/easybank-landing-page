<script setup>
defineProps({
    padded: {
        type: Boolean,
        default: true,
    },
})
</script>
<template>
    <section :class="{'padded': padded}">
        <div class="content">
            <slot></slot>
        </div>
    </section>
</template>
<style scoped lang="scss">
@use '@/assets/base.scss' as *;

section {
    position: relative;
    background-color: var(--very-light-gray);

    &.padded {
        padding: 3rem 1rem;
    }

    &:nth-of-type(even) {
        background-color: var(--light-grayish-blue);
    }

    .content {
        max-width: $content-width;
        margin: 0 auto;
    }
}
</style>