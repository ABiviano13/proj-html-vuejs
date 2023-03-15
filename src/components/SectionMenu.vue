<script>
import CardMenu from './CardMenu.vue';

export default {
    components: {
        CardMenu
    },
    data() {
        return{
            menuCards: [
                {
                    src: 'src/assets/images/appetizers-menu-background.jpg',
                    text: 'Appetizers'
                },
                {
                    src: 'src/assets/images/burgers-menu-background.jpg',
                    text: 'Burgers'
                },
                {
                    src: 'src/assets/images/pizza-menu-background.jpg',
                    text: 'Pizzas'
                },
                {
                    src: 'src/assets/images/fries-menu-background.jpg',
                    text: 'Fries'
                },
                {
                    src: 'src/assets/images/sides-menu-background.jpg',
                    text: 'Sides'
                },
                {
                    src: 'src/assets/images/desserts-menu-background.jpg',
                    text: 'Desserts'
                },
                {
                    src: 'src/assets/images/beverages-menu-background.jpg',
                    text: 'Beverages'
                },
                {
                    src: 'src/assets/images/specials-menu-background.jpg',
                    text: 'Specials'
                }
            ]
        }
    }
    
}
</script>

<template>
    <section class="menu-categories">
        <div class="container">
            <div class="row-button">
                <button class="button">
                    View the full menu
                    <i class="fa-solid fa-circle-arrow-right"></i>
                </button>
            </div>
            <h1 class="title">
                Menu Categories
            </h1>
            <div class="cards-menu">
                <CardMenu
                v-for="menu in menuCards" :key="menu.src"
                :imageCard="menu.src"
                :textCard="menu.text"
                ></CardMenu>
            </div>
            <div class="icons-characteristics">
                <div class="icon">
                    <i class="fa-solid fa-leaf"></i>
                    <div class="text-icon">
                        Vegetarian
                    </div>
                </div>
                <div class="icon">
                    <i class="fa-solid fa-wheat-awn"></i>
                    <div class="text-icon">
                        Gluten Free
                    </div>
                </div>
                <div class="icon">
                    <i class="fa-solid fa-cow"></i>
                    <div class="text-icon">
                        Dairy Free
                    </div>
                </div>
                <div class="icon">
                    <i class="fa-solid fa-drumstick-bite"></i>
                    <div class="text-icon">
                        Keto Friendly
                    </div>
                </div>
            </div>
        </div>
        <div class="ordering-app">
            <div class="text-app">

                <div class="text-small">
                    Download Our 
                </div>
                <div class="text-big">
                    Ordering App
                </div>
                <div class="app">
                    <img src="../assets/images/app-store-badge.png" alt="app-store">
                    <img src="../assets/images/play-store-badge.png" alt="play-store">
                </div> 

            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables.scss' as *;
.menu-categories{

    .row-button{
        display: flex;
        justify-content: end;
    }


    .cards-menu {
        display: grid;
        grid-template-columns: repeat(4, 2fr);
        gap: 20px;
        margin-top: 60px;
        margin-bottom: 75px;
    }

    .icons-characteristics{
        display: flex;
        justify-content: space-around;

        .icon{
            text-align: center;
            
            i {
                font-size: 67px;
                padding-bottom: 14px;
            }

            .text-icon{
                font-weight: bold;
            }

            .fa-leaf{
                color: $green;
            }

            .fa-wheat-awn{
                color: $yellow;
            }

            .fa-cow{
                color: $lightblue;
            }

            .fa-drumstick-bite{
                color: $brown;
            }

        }
    }

    .ordering-app{
        background-image: url('../assets/images/app-ordering-scaled.jpg');
        background-size: cover;
        height: 575px;
        margin-top: 149px;
        font-weight: bold;
        position: relative;

        .text-app{
            position: absolute;
            top: 137px;
            left: 361px;

            .text-small{
                font-size: 33px;
                color: $white
            }

            .text-big{
                font-size: 82px;
                color: $yellow;
            }

            .app{
                display: flex;
                gap: 26px;
                height: 54px;
                margin-top: 61px;
            }
        }
    }
}

</style>