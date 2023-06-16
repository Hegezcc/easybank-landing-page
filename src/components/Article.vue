<script setup>
defineProps({
    title: String,
    img: String,
    author: String,
})
</script>
<template>
    <article>
        <img :src="img" :alt="title" />
        <p class="author">By {{ author }}</p>
        <h2>
            <a href="#">{{ title }}</a>
        </h2>
        <p class="body">
            <slot></slot>
        </p>
    </article>
</template>

<style scoped lang="scss">
article {
    background-color: var(--white);
    border-radius: 0.5rem;
    box-shadow: 0 0 0.5rem var(--light-grayish-blue);
    overflow: hidden;
    margin: 1rem 0; 
    text-align: left;

    img {
        width: 100%;
        height: 50%;
        object-position: center;
        object-fit: cover;
    }

    .author {
        color: var(--grayish-blue);
        font-size: 0.5rem;
        margin: 0.5rem 1rem;
    }

    h2 {
        margin: 0 1rem;
        font-size: 1rem;
    }

    .body {
        margin: 0.5rem 1rem 1rem 1rem;
        color: var(--grayish-blue);
        font-size: 0.7rem;
        line-height: 1.3;
    }
}
</style>