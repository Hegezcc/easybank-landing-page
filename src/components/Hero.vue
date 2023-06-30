<script setup>
import InviteButton from './InviteButton.vue'
import SectionBase from './SectionBase.vue'
import MockupImage from '@/assets/images/image-mockups.png'
</script>
<template>
    <SectionBase :padded="false">
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
    </SectionBase>
</template>

<style scoped lang="scss">
@use '@/assets/base.scss' as *;

.image {
    position: relative;
    background: url('@/assets/images/bg-intro-mobile.svg') no-repeat center bottom;
    background-size: cover;

    img {
        display: block;
        width: 100%;
        margin: -35% 0 15% 0;
    }
}

.container {
    display: flex;
    flex-direction: column-reverse;
    max-width: $content-width;
}

.content {
    margin: -3rem 0 5rem 0;
    padding: 0 1rem;

    p {
        color: var(--grayish-blue);
        font-size: 0.8rem;
        margin-bottom: 2rem;
    }
}

@media screen and (min-width: $desktop-min) {
    .image {
        background: url("/src/assets/images/bg-intro-desktop.svg") 12% 85%/90vw no-repeat;
        width: 50vw;
        height: 50vw;
        position: absolute;
        right: 0;
        z-index: 1;
        overflow-x: clip;

        img {
            margin: 0;
            position: relative;
            top: -9%;
            right: -17%;
        }
    }

    .container {
        flex-direction: row;
        min-height: 50vw;
        align-items: center;
    }

    .content {
        text-align: left;
        width: calc(50% - 5rem);
        margin: 0;

        p {
            font-size: 1rem;
        }
    }

    h1 {
        font-size: 3rem;
    }
}
</style>