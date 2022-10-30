<template>
    <div>
        <img src="./heroImage.png" alt="Hero Image for the wave app">
    </div>
</template>

<style scoped>

    img {
        position: fixed;
        width: 80vw;
        /* margin-top: 5%; */
        bottom: 0;
        margin: 0;
        filter: drop-shadow(0px 8px 8px rgba(0, 0, 0, 0.612));
    }

    @media (min-width: 500px) {
        img {
            width: 60vw;
        }
    }

    @media (min-width: 1024px) {
        img {
            width: 35vw;
        }
    }

    @media (min-width: 1920px) {
        img {
            width: 30vw;
            /* top: 3vh;  */
        }
    }  
</style>