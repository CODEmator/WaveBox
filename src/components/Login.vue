<script setup>
import LoginItem from './LoginItem.vue'
import LoginImage from './images/LoginImage.vue'
import LoginForm from './LoginForm.vue'
</script>

<template>
    <LoginItem>
        <template #image>
            <LoginImage/>
        </template>
        <template #form>
            <LoginForm/>
        </template>
    </LoginItem>
</template>
