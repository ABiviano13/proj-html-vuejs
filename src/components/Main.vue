<script>
import PopularDishes from './PopularDishes.vue';
import Menu from './Menu.vue';

export default {
    components: {
        PopularDishes,
        Menu
    },
    data() {
        return {
        
        }
    }
}
</script>

<template>
    <PopularDishes></PopularDishes>
    <Menu></Menu>
</template>

<style lang="scss" scoped>
*{
    color: black;
}
</style>