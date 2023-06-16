<script setup>
import { ref } from 'vue'
import InviteButton from './InviteButton.vue'

const navOpen = ref(false)
let lastOpen = null;

const toggleNav = () => {
    // Use lastOpen timestamp to prevent multi clicks with 100ms limiter
    if (lastOpen === null || lastOpen < Date.now() - 100) {
        lastOpen = Date.now();
        navOpen.value = !navOpen.value;
    }
}
</script>
<template>
    <header :class="{'active': navOpen}" id="header">
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
    <div class="header-space"></div>
    <div class="nav-closer" v-if="navOpen" @click.prevent="toggleNav"></div>
</template>

<style scoped lang="scss">
@use '@/assets/base.scss' as *;

header {
    position: fixed;
    display: flex;
    top: 0;
    left: 0;
    right: 0;
    height: 3rem;
    z-index: 11;
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
        z-index: 12;
    }

    & > * {
        z-index: 12;
        margin: 1rem;
    }

    img {
        flex: 0 0 auto;
        margin: auto 1rem;
    }

    .invite-button {
        display: none;
    }

    .nav-icon {
        display: block;
        padding: 1rem;
        margin: 0;
        font-size: 1rem;
        border: none;
        background: none;
        height: 3rem;

        img {
            width: 1.3rem;
            height: 1rem;
            object-fit: contain;
            margin: 0;
        }
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
        z-index: 11;

        a {
            display: block;
            color: var(--dark-blue);
            text-decoration: none;
            padding: 0.5rem;
        }
    }

    &.active nav {
        display: block;
        opacity: 1;
    }
}

.header-space {
    height: 3rem;
}

.nav-closer {
    position: fixed;
    z-index: 11;
    bottom: 0;
    right: 0;
    left: 0;
    top: 3rem;
}

@media screen and (min-width: $desktop-min) {
    header {
        height: 5rem;
        .nav-icon {
            display: none;
        }

        nav {
            position: static;
            display: block;
            opacity: 1;
            margin: 0;
            padding: 0;
            border-radius: 0.25rem;
            box-shadow: none;
            z-index: 12;

            ul {
                display: flex;
                height: 100%;

                li {
                    position: relative;
                    display: flex;
                    align-items: center;

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

    .header-space {
        height: 5rem;
    }

    .nav-closer {
        display: none;
    }
}

</style>