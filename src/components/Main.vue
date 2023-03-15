<script>

import SectionPopularDishes from './SectionPopularDishes.vue';
import SectionMenu from './SectionMenu.vue';
import SectionNews from './SectionNews.vue';

export default {
    components: {
        SectionPopularDishes,
        SectionMenu,
        SectionNews
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
    <SectionNews></SectionNews>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables.scss' as *;

*{
    color: $black;
}
</style>