<template>
    <form action="" method="get">
        <h1>Login</h1><br><br>
        <div class="line"></div>
        <div class="input-control">
            <label for="email">Email</label>
            <input id="email" name="email" type="text">
            <div class="error"></div>
        </div>
        <div class="input-control">
            <label for="password">Password</label>
            <input id="password" name="password" type="password">
            <i class="fas fa-eye-slash createShow"></i>
            <div class="error"></div>
        </div>
        <div class="link">
            <RouterLink to="/">Forget Password?</RouterLink>
        </div><br>
        <input type="submit" value="Login">
        <div class="link">
            Don't have an account?
            <RouterLink to="./join" id="joinNow"> Join Now</RouterLink>
        </div><br>
    </form>

</template>

<style scoped>
form {
    display: block;
    background-color: var(--vt-c-white);
    padding: .5rem;
    border-radius: 1rem;
    margin: .3rem auto;
    width: 80vw;
    box-sizing: border-box;
}

h1 {
    font-size: 1.5rem;
    font-weight: bold;
}

label {
    font-size: 1rem;
}

input {
    border: .2rem solid var(--vt-c-white-nude);
    border-radius: 10px;
    display: block;
    font-size: .8rem;
    padding: .5rem;
    width: 100%;
}

input:focus {
    outline: 0%;
}

input[type=submit] {
    width: 100%;
    font-size: 1rem;
    color: var(--vt-c-white);
    background-color: var(--vt-c-blue);
    /* border: var(--vt-c-white); */
}


.input-control {
    display: flex;
    flex-direction: column;
}

i {
    position: absolute;
    display: flex;
    margin-top: 11%;
    margin-left: 92%;
    color: var(--vt-c-blue);
    /* background-color: var(--vt-c-white-nude); */
    place-items: center;
    justify-content: center;
}

.link {
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: .2rem;
    margin-top: .4rem;
    font-size: .8rem;
}

a {
    color: var(--vt-c-blue);
}

@media (hover: hover) {
  a:hover {
    color: var(--vt-c-pink);
  }

    input[type=submit]:hover {
        font-weight: bold;
        letter-spacing: 2px;
        background-color: var(--vt-c-white);
        color: var(--vt-c-blue);
        border-color: var(--vt-c-blue);
    }
}
@media (min-width: 1024px) {
    form {
        width: 100%;
    }

    i {
        margin-top: 10%;
    }
}
</style>