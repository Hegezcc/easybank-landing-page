<script setup>
import InviteButton from './InviteButton.vue'

</script>
<template>
    <header>
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
        <InviteButton />
    </header>
</template>

<style scoped lang="scss">

header {
    display: flex;
    background-color: var(--white);
    color: var(--dark-blue);

    img {
        flex: 0 0 auto;
    }
}

</style>