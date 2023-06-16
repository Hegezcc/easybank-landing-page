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
    margin: 1rem; 

    img {
        width: 100%;
    }

    .author {
        color: var(--grayish-blue);
        font-size: 0.5rem;
        margin: 0.5rem 2rem;
    }

    h2 {
        margin: 0 2rem;
        font-size: 1rem;

        a {
            color: var(--dark-blue);
            text-decoration: none;

            &:hover, &:active {
                color: var(--lime-green);
            }
        }
    }

    .body {
        margin: 0.5rem 2rem 2rem 2rem;
        color: var(--grayish-blue);
        font-size: 0.6rem;
        line-height: 1.3;
    }
}
</style>