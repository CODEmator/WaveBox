<script setup>
import JoinItem from './JoinItem.vue'
import JoinForm from './JoinForm.vue'
</script>

<template>
    <JoinItem>
        <template #heading>Join the</template>
        <template #pink> fun</template>
        <template #form>
            <JoinForm/>
        </template>
    </JoinItem>
</template>

