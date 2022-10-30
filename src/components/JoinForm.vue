
<template>
    <form action="" method="post">
        <div class="input-control">
            <label for="username">Username</label>
            <input id="username" name="username" type="text">
            <div class="error"></div>
        </div>
        <div class="input-control">
            <label for="email">Email</label>
            <input id="email" name="email" type="text">
            <div class="error"></div>
        </div>
        <div class="input-control">
            <label for="create_pw">Create Password</label>
            <input id="create_pw" name="create_pw" type="password">
            <i class="fas fa-eye-slash createShow"></i>
            <div class="error"></div>
        </div>
        <div class="input-control">
            <label for="confirm_pw">Confirm Password</label>
            <input id="confirm_pw" name="confirm_pw" type="password">
            <i class="fas fa-eye-slash confirmShow"></i>
            <div class="error"></div>
        </div>
        <div class="link">
            <p>Already have an account?
                 <RouterLink to="/login">Log In</RouterLink>
            </p>
        </div><br>
        <input class="button" type="submit" value="Create Account">
        <div class="footnote">By clicking Create Account you agree to our 
            <RouterLink to="/">Terms and Conditions</RouterLink> and 
            <RouterLink to="/">Privacy Policy</RouterLink>
        </div>
    </form>
</template>
<style scoped>
form {
    display: block;
    background-color: var(--vt-c-white-mute);
    padding: 1rem;
    border-radius: 1rem;
    margin: 2rem auto;

}

.input-control {
    display: flex;
    flex-direction: column;
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
    outline: 0;
}

input[type=submit] {
    font-size: 1.2rem;
    padding: .4rem;
    margin-top: .5rem;
    width: 100%;
    color: var(--vt-c-white-mute);
    background-color: var(--vt-c-blue);
    border: none;
    border-radius: 10px;
}

a {
    color: var(--vt-c-blue);
}

.link,.footnote {
    align-items: center;
    text-align: center;
    font-size: 1rem;
    margin: 1rem auto;
}

p {
    font-size: 1rem;
}

i {
    position: absolute;
    display: flex;
    top: 64%;
    left: 90%;
    /* z-index: 1; */
    place-items: center;
    justify-content: center;
}

@media (hover: hover) {
  a:hover {
    color: var(--vt-c-pink);
  }
}

@media (min-width: 1024px) {
    form {
        width: 75%;
        padding: 5%;
    }

    label {
        font-size: 1.4rem;
    }

    input {
        font-size: 1.2rem;
        padding: .7rem;
    }

    input[type=submit] {
        font-size: 1.4rem;
        padding: .6rem;
    }
}
</style>

<!-- <script src="../form.js"></script> -->