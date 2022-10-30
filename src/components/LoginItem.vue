<template>
    <div class="container">
        <div class="left">
            <slot name="image"></slot>
        </div>
        <div class="right">
            <slot name="form"></slot>
        </div>
    </div>
</template>

<style scoped>
.container {
    display: flex;
    flex-direction: row;
    position: absolute;
    z-index: 999;
    width: 100%;
    align-items: center;
    justify-content: center;
    align-content: center;
    top: 50vh;
    transform: translateY(-50%);
    background-color: var(--vt-c-white);
    border-radius: 1.4rem;
}

</style>