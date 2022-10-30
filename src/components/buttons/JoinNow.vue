<script setup>
import { RouterLink } from 'vue-router'
</script>

<template>
    <div class="button">
        <RouterLink to="/join">Join Now</RouterLink>
    </div>
</template>

<style scoped>
    .button {
        display: block;
        min-width: max-content;
        max-width: max-content;
        font-size: 1.6rem;
        padding: 0.4rem 0.6rem;
        background-color: var(--color-heading);
        border-radius: .6rem;
        box-sizing: border-box;
    }

@media (hover: hover) {
    .button:hover {
        background-color: transparent;
        /* color: var(--vt-c-pink); */
        box-shadow: 0 12px 16px 0 rgba(0,0,0,0.24), 0 17px 50px 0 rgba(0,0,0,0.19);
    }
}
</style>
