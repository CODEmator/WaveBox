<template>
    <div class="container">
        <div class="left">
            <h1>
                <slot name="heading"></slot>
                <span><slot name="pink"></slot></span>
            </h1>
        </div>
        <div class="right">
            <slot name="form"></slot>
        </div>
    </div>
</template>

<style scoped>
    .container {
        display: flex;
        flex-direction: column;
        margin: 1rem auto;
    }

    h1 {
        font-size: 2.5rem;
        font-weight: 600;
    }

    span {
        color: var(--vt-c-pink);
        font-weight: bolder;
        font-size: 2.8rem;
    }

    .right {
        width: 100%;
    }

@media (min-width: 1024px) {
    .container {
        display: grid;
        grid-template-columns: 40vw 40vw;
        justify-content: space-between;
        align-items: center;
        margin: 2rem auto;
        /* gap: 15vw; */
    }

    .left {
        display: flex;
        flex-direction: row;
        align-items: flex-end;
        margin-left: -3rem; 
    }

    h1 {
        font-size: 3.8rem;
    }

    span {
        font-size: 4rem;
    }

    .right {
        display: flex;
        flex-direction: row;
        align-items: flex-start;
        /* right: -25vw; */
        /* width: 30vw; */
    }
}
</style>