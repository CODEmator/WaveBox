<template>
    <div class="container">
        <div class="left">
            <h1>
                <slot name="heading"></slot>
            </h1>
            <div class="gridbox">
                <div class="grid">
                    <i>
                        <slot name="icon"></slot>
                    </i>
                    <h3>
                        <slot name="iconName"></slot>
                    </h3>
                </div>
                <div class="grid">
                    <i>
                        <slot name="icon2"></slot>
                    </i>
                    <h3>
                        <slot name="iconName2"></slot>
                    </h3>
                </div>
                <div class="grid">
                    <i>
                        <slot name="icon3"></slot>
                    </i>
                    <h3>
                        <slot name="iconName3"></slot>
                    </h3>
                </div>
            </div>
            <p>
                <slot name="text"></slot>
                <span><slot name="italic"></slot></span>
            </p>
        </div>
        <div class="right">
            <div class="imgGrid">
                <slot name="discoverImg"></slot>
            </div>
        </div>
    </div>
</template>

<style scoped>

    .container {
        display: block;
        place-items: center;
    }
    .left {
        margin-top: 1rem auto;
    }
    h1 {
        font-size: 2.4rem;
        font-weight: 700;
        color: var(--vt-c-black-soft);
    }

    .gridbox {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    .grid {
        display: flex;
        flex-direction: column;
        width: 20vw;
        background-color: var(--vt-c-black-soft);
        padding: .8rem;
        place-items: center;
    }

    h3 {
        color: var(--vt-c-text-dark-2);
        font-size: 1.5rem;
        font-weight: bold;
        text-align: center;
    }

    p {
        font-size: 1.3rem;
        color: var(--vt-c-black-soft);
    }

    span {
        font-weight: bolder;
        font-style: italic;
    }

    .right {
        display: flex;
        place-items: center;
        margin: 2rem auto;
        /* right: -2rem; */
    }

    .imgGrid {
        display: flex;
        align-items: center;
    }

@media (min-width: 700px) {
    .right {
        right: -2rem;
    }
}

@media (min-width: 1024px) {
    .container {
        display: grid;
        grid-template-columns: 40vw 50vw;
        justify-content: space-between;
        align-items: flex-start;
        margin: 2.6rem auto;
        /* max-width: 100vw; */
    }

    h1 {
        font-size: 3rem;
    }

    h3 {
        font-size: 2rem;
    }

    p {
        font-size: 1.8rem;
    }

    span {
        font-weight: bolder;
        font-style: italic;
    }

    .left {
        align-items: flex-start;
    }

    .grid {
        width: 20%;
    }
}

</style>