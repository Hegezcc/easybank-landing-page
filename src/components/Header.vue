<script setup>
import { ref } from 'vue'
import InviteButton from './InviteButton.vue'

const navOpen = ref(false)

const toggleNav = () => {
    navOpen.value = !navOpen.value
}
</script>
<template>
    <header :class="{'active': navOpen}">
        <img src="@/assets/images/logo.svg" alt="Easybank" />
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Contact</a></li>
                <li><a href="#">Blog</a></li>
                <li><a href="#">Careers</a></li>
            </ul>
        </nav>
        <button class="nav-icon" @click.prevent="toggleNav">
            <img v-if="navOpen" src="@/assets/images/icon-close.svg" alt="Close Navigation" />
            <img v-else src="@/assets/images/icon-hamburger.svg" alt="Open Navigation" />
        </button>
        <InviteButton />
    </header>
</template>

<style scoped lang="scss">
@use '@/assets/base.scss' as *;

header {
    position: relative;
    display: flex;
    background-color: var(--white);
    color: var(--dark-blue);
    justify-content: space-between;

    &::before {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        background: var(--white);
        z-index: 2;
    }

    & > * {
        z-index: 2;
        margin: 1rem;
    }

    img {
        flex: 0 0 auto;
    }

    .invite-button {
        display: none;
    }

    .nav-icon {
        display: block;
        padding: 0;
        font-size: 1rem;
        border: none;
        background: none;
    }

    nav {
        position: absolute;
        display: none;
        opacity: 0;
        top: 100%;
        left: 0;
        right: 0;
        background: var(--white);
        padding: 1rem;
        margin: 1rem;
        border-radius: 0.25rem;
        box-shadow: 0 0 10rem var(--dark-blue);
        z-index: 1;

        a {
            display: block;
            color: var(--dark-blue);
            text-decoration: none;
            text-align: center;
            padding: 0.5rem;
        }
    }

    &.active nav {
        display: block;
        opacity: 1;
    }
}

@media screen and (min-width: $desktop-min) {
    header {
        .nav-icon {
            display: none;
        }

        nav {
            position: static;
            display: block;
            opacity: 1;
            margin: 1rem 0 0 0;
            padding: 0;
            border-radius: 0.25rem;
            box-shadow: none;
            z-index: 2;

            ul {
                display: flex;
                height: 100%;

                li {
                    position: relative;

                    &::before {
                        content: '';
                        display: none;
                        position: absolute;
                        bottom: 0;
                        right: 0;
                        left: 0;
                        height: 0.25rem;
                        background: var(--lime-green);
                    }

                    &:hover {
                        &::before{
                            display: block;
                        }

                        a {
                            color: var(--dark-blue);
                        }
                    }

                    a {
                        color: var(--grayish-blue);
                    }
                }
            }
        }

        .invite-button {
            display: block;
        }
    }
}

</style>