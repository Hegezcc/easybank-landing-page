<script setup>
import InviteButton from './InviteButton.vue'
import MockupImage from '@/assets/images/image-mockups.png'
</script>
<template>
    <div class="container">
        <div class="content">
            <h1>Next generation digital banking</h1>
            <p>
                Take your financial life online. Your Easybank account will be a one-stop-shop 
                for spending, saving, budgeting, investing, and much more.
            </p>
            <InviteButton></InviteButton>
        </div>
        <div class="image">
            <img :src="MockupImage" alt="Mockups" />
        </div>
    </div>
</template>

<style scoped>
.image {
    background: url('@/assets/images/bg-intro-mobile.svg') no-repeat;
}

@media screen and (min-width: 720px) {
    .image {
        background: url('@/assets/images/bg-intro-desktop.svg') no-repeat;
    }
}
</style>