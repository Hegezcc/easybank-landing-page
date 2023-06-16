<script setup>
defineProps({
    title: String,
    img: String,
})
</script>
<template>
    <div class="point">
        <img :src="img" :alt="title" />
        <h3>{{ title }}</h3>
        <p class="body">
            <slot></slot>
        </p>
    </div>
</template>
<style scoped lang="scss">
.point {
    margin-top: 3rem;
}

p {
    color: var(--grayish-blue);
}
</style>