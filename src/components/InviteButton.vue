<template>
    <button class="invite-button">Request Invite</button>
</template>
<style scoped lang="scss">
@use '@/assets/base.scss' as *;

button {
    margin: 0;
    padding: 0.75rem 1.5rem;
    border: none;
    border-radius: 2rem;
    font-size: 0.8rem;
    color: var(--white);
    background: var(--main-gradient);
}

button:hover, button:active {
    cursor: pointer;
    background: var(--light-gradient);
}

@media screen and (min-width: $desktop-min) {
    button {
        font-size: 1rem;
    }
}
</style>