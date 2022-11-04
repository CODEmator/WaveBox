<template>
    <div class="container">   
        <div class="inner">
            <div class="left">
                <slot name="image"></slot>
            </div>
            <div class="right">
                <slot name="form"></slot>
            </div>
        </div>
    </div>
</template>

<style scoped>
.container {
    width: 100%;
    height: auto;
    place-items: center;
    margin: 0;
    padding: auto;
    margin-bottom: 28vh;
}
.inner {
    display: flex;
    flex-direction: row;
    width: 100%;
    top: 15vh;
    /* align-items: center;
    place-self: center; */
    /* justify-content: space-between; */
    background-color: var(--vt-c-white);
    border-radius: 1.4rem;
}
@media (min-width: 1024px) {
    .inner {
        display: grid;
        grid-template-columns: 50% 50%;
        justify-content: space-between;
    }

    .left {
        background-color: var(--vt-c-white-nude);
        border-radius: 1.4rem 0 0 1.4rem;
    }
    .right {
        margin: .6rem;
        
    }
}
</style>