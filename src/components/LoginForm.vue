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
            <label for="create_pw">Password</label>
            <input id="create_pw" name="create_pw" type="password">
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
    padding: .2rem;
    border-radius: 1rem;
    margin: .3rem auto;
    width: 80vw;
}

h1 {
    font-size: 1.8rem;
    font-weight: bold;
}

label {
    font-size: 1.2rem;
}

input {
    border: .2rem solid var(--vt-c-white-nude);
    border-radius: 10px;
    display: block;
    font-size: 1rem;
    padding: .5rem;
    width: 100%;
}

input:focus {
    outline: 0%;
}

input[type=submit] {
    width: 100%;
    font-size: 24px;
    color: var(--vt-c-white);
    background-color: var(--vt-c-blue);
    /* border: var(--vt-c-white); */
}

input[type=submit]:hover {
    letter-spacing: 2px;
    background-color: var(--vt-c-white);
    color: var(--vt-c-blue);
    border-color: var(--vt-c-blue);
}

.input-control {
    display: flex;
    flex-direction: column;
}

i {
    position: absolute;
    display: flex;
    top: 46%;
    left: 88%;
    /* z-index: 1; */
    background-color: var(--vt-c-white-nude);
    width: 8vw;
    height: 4%;
    place-items: center;
    justify-content: center;
    border: .2rem solid var(--vt-c-white-nude);
    border-radius: 0 6px 6px 0;
}

.link {
    align-items: center;
    justify-content: center;
    text-align: center;
    padding: .2rem;
    margin-top: .4rem;
}

a {
    color: var(--vt-c-blue);
}

@media (hover: hover) {
  a:hover {
    color: var(--vt-c-pink);
  }
}
</style>