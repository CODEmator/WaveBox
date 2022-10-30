<template>
  <div class="container">
    <div name="left">
      <div class="design1">
        <slot name="design1"></slot>
      </div>
      <div class="heroImg">
        <slot name="heroImg"></slot>
      </div>
    </div>
    
    <div class="right">
      <h1>
        <slot name="heading"></slot>
      </h1>
      <h3>
        <slot name="text"></slot>
      </h3>
      <div class="button">
        <slot name="button"></slot>
      </div>
      <div class="design2">
        <slot name="design2"></slot>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container{
  display: flex;
  flex-direction: column-reverse;
}

.button {
  place-content: center;
  place-items: center;
  /* margin-left: 50vw; */
}

.right {
  display: flex;
  flex-direction: column;
  place-items: left;
  /* place-content: center; */
  top: 15vh;
}

h1 {
  font-size: 2.8rem;
  font-weight: 700;
}

h3 {
  font-size: 1.2rem;
  font-weight: 500;
  margin-bottom: 0.4rem;
  color: var(--color-heading);
}

.design1 {
  position: fixed;
  left: 0;
  bottom: -1vh;
  margin: 0;
  padding: 0;
}

.design2 {
  position: fixed;
  z-index: -5;
  right: 0;
  top: -35vh;
}

@media (min-width: 500px) {
  .right {
    text-align: center;
    place-items: center;
  }

  .button {
    min-width: max-content;
    /* left: 40%; */
  }

  h1 {
    font-size: 3.4rem;
  }

  h3 {
    font-size: 2rem;
  }
}

@media (min-width: 1024px) {
  .container {
    display: grid;
    grid-template-columns: 45vw 45vw;
    align-items: left;
    justify-content: space-between;
    margin-top: 0.5rem;
    margin-bottom: 0;
    padding: 0.4rem 0 1rem 0;
  } 
  .right {
    place-items: start;
    text-align: left;
    top: 25vh;
    margin-left: 10vw;
  }

  .button {
    left: 0;
  }
  .design2 {
    top: auto;
    bottom: -20vh;
  }

  h1 {
    text-align: left;
    font-size: 4rem;
    font-weight: 700;
    margin-bottom: 0;
    margin-top: -10vh;
  }

  h3 {
    text-align: left;
    font-size: 2.2rem;
    margin-top: -1rem;
    margin-bottom: 0.4rem;
    color: var(--color-heading);
  } 
   
}
</style>
