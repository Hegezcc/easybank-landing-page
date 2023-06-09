<script setup>
import { defineProps } from 'vue'
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
        <h2>{{ title }}</h2>
        <p class="body">
            <slot></slot>
        </p>
    </article>
</template>