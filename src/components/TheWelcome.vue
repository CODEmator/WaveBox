<script setup>
import WelcomeItem from './WelcomeItem.vue'
import HeroImg from './images/HeroImage.vue'
import JoinBtn from './buttons/JoinNow.vue'
import DesignOne from '../components/icons/HeroDesign1.vue'
import DesignTwo from '../components/icons/HeroDesign2.vue'

</script>

<template>
  <WelcomeItem>
    <template #design1>
      <DesignOne/>
    </template>
    <template #heroImg>
      <HeroImg/>
    </template>
    <template #heading>Feel The Music</template>
    <template #text >Stream over 20k+ songs with a click</template>
    <template #button>
      <JoinBtn/>
    </template>
    <template #design2>
      <DesignTwo/>
    </template>
  </WelcomeItem>
</template>
