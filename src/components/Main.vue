<script>

import SectionPopularDishes from './SectionPopularDishes.vue';
import SectionMenu from './SectionMenu.vue';

export default {
    components: {
        SectionPopularDishes,
        SectionMenu
    },
    data() {
        return {
        
        }
    }
}

</script>

<template>
    <SectionPopularDishes></SectionPopularDishes>
    <SectionMenu></SectionMenu>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables.scss' as *;

*{
    color: $black;
}
</style>