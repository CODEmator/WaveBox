<script setup>
import DiscoverItem from './DiscoverItem.vue'
import DiscoverImg from './images/DiscoverImage.vue'
import IconChart from './icons/IconCharts.vue'
import IconAlbum from './icons/IconAlbum.vue'
import IconMore from './icons/IconMore.vue'
</script>

<template>
    <DiscoverItem>
        <template #heading>Discover New Music</template>
        <template #icon>
            <IconChart/>
        </template>
        <template #iconName>Charts</template>
        <template #icon2>
            <IconAlbum/>
        </template>
        <template #iconName2>Album</template>
        <template #icon3>
            <IconMore/>
        </template>
        <template #iconName3>More</template>
        <template #text>
            “Music gives a soul to the universe, wings to the mind, flight to the imagination and life to everything.”
        </template>
        <template #italic> ― Plato</template>
        <template #discoverImg>
            <DiscoverImg/>
        </template>
    </DiscoverItem>
</template>