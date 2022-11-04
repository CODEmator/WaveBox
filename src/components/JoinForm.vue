<script>
import useValidate from '@vuelidate/core'
import { required, email, minLength, sameAs } from '@vuelidate/validators'
import { reactive, computed } from 'vue'
export default {
    //....
    setup() {
        const state = reactive( {
            username: '',
            email: '',
            password: {  
                create_pw: '',       
                confirm_pw: '',      
            },    
        })
        const rules = computed( () => {
            return {
                username: { required }, 
                email: { required, email },
                password: { 
                    create_pw: { required, minLength: minLength(8) },
                    confirm_pw: { required, sameAs: sameAs(state.password.create_pw) },
                }
            }
        })
        const v$ = useValidate(rules, state)    
        return { state, v$ }
    },
    // .....
    methods: {
        submitForm() {
            this.v$.$validate() /*....Checks all inputs....*/ 
            if (!this.v$.$error) {
                //.... if ANY fail validation
                alert('Account Form Successfully Submitted') 
            } 
            else {
                alert('Account Form Failed Validation')
            }
            
        }
    },
    // ......
    validations() {
        return {}
    },
}
</script>

<template>
    <form action="" method="post">
        <div class="input-control">
            <label for="username">Username</label>
            <input id="username" name="username" type="text" v-model="state.username">
            <div class="error" v-if="v$.username.$error"> {{ v$.username.$errors[0].$message }}</div>
        </div>
        <div class="input-control">
            <label for="email">Email</label>
            <input id="email" name="email" type="text" v-model="state.email">
            <div class="error" v-if="v$.email.$error"> {{ v$.email.$errors[0].$message }}</div>
        </div>
        <div class="input-control">
            <label for="create_pw">Create Password</label>
            <input id="create_pw" name="create_pw" type="password" v-model="state.password.create_pw">
            <i class="fas fa-eye-slash createShow"></i>
            <div class="error" v-if="v$.password.create_pw.$error"> {{ v$.password.create_pw.$errors[0].$message }}</div>
        </div>
        <div class="input-control">
            <label for="confirm_pw">Confirm Password</label>
            <input id="confirm_pw" name="confirm_pw" type="password" v-model="state.password.confirm_pw">
            <i class="fas fa-eye-slash confirmShow"></i>
            <div class="error" v-if="v$.password.confirm_pw.$error"> {{ v$.password.confirm_pw.$errors[0].$message }}</div>
        </div>
        <div class="link">
            <p>Already have an account?
                 <RouterLink to="/login">Log In</RouterLink>
            </p>
        </div><br>
        <input @click="submitForm" class="button" type="button" value="Create Account">

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
    width: 100%;
}

.input-control {
    display: flex;
    flex-direction: column;
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
    outline: 0;
}

input[type=button] {
    font-size: 1rem;
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
    font-size: .8rem;
    margin: 1rem auto;
}

p {
    font-size: .8rem;
}

i {
    position: absolute;
    display: flex;
    margin-top: 10%;
    margin-left: 91%;
    color: var(--vt-c-blue);
    place-items: center;
    justify-content: center;
}

.error {
    color: red;
    font-size: 10px;
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
        font-size: 1rem;
    }

    input {
        font-size: 1rem;
        padding: .7rem;
    }

    input[type=button] {
        font-size: 1.2rem;
        padding: .6rem;
    }
    
    i {
        position: absolute;
        display: flex;
        margin-top: 9%;
        margin-left: 93%;
        color: var(--vt-c-blue);
        place-items: center;
        justify-content: center;
    }
}
</style>

<!-- <script src="../form.js"></script> -->