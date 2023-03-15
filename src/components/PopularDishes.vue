<script>
import CardPopularDishes from './CardPopularDishes.vue';

export default {
    components:{
        CardPopularDishes
    },
    data() {
        return {
            dishes: [
                {
                    src: 'src/assets/images/skin-on-fries.jpg',
                    text: 'Skin On Fries',
                    price: '$3.00 - $6.00'
                },
                {
                    src: 'src/assets/images/choco-cookie-frappe.jpg',
                    text: 'Choco Cookie Frappe',
                    price: '$4,99'
                },
                {
                    src: 'src/assets/images/donut-burger.jpg',
                    text: 'The Donut Burger',
                    price: '$6,99'
                }
            ]
        }
    }
}
</script>

<template>
    <section class="popular-dishes">
        <div class="container">
            <h1>
                Our Most Popular Dishes
            </h1>

            <div class="cards-dishes">
                <CardPopularDishes
                v-for="dish in dishes"
                :imageCard="dish.src"
                :textCard="dish.text"
                :priceCard="dish.price"
                >
                </CardPopularDishes>
            </div>
            <button class="button">
                Start your order
                <i class="fa-solid fa-circle-arrow-right"></i>
            </button>
        </div>
        <svg class="fusion-waves-opacity-candy" fill="#fff" xmlns="http://www.w3.org/2000/svg" viewBox="3 0 1000 350" preserveAspectRatio="none"><path class="st0" d="M0 215.4c19.4.5 38.7 1.6 57.7.3 206.6-15 248.5-126.6 455-143.8 184.8-15.5 285.7 60.9 464.3 41.3 16.9-1.8 32.5-4.4 47.1-7.6L1024 .4H0v215z"/><path class="st1" d="M0 196.4c30.2 1.6 59.6 1.6 86.8-.4C293.4 180.9 284.1 73.4 490.7 56.2c184.9-15.5 278.5 58.2 457.1 38.4 28.3-3.2 53.5-8.2 76.2-14.6V.256H0V196.4z"/><path class="st2" d="M0 169.8c22.2.3 43.8-.2 64.2-1.7C270.8 153.1 262 55.6 468.6 38.4 653.4 22.9 695.4 89.5 874 69.7c54.8-6 104.9-18.3 150-33.7V.256H0V169.8z"/><path class="st3" d="M0 162.1c4-.2 8-.4 11.9-.7C218.4 146.3 239.8 37 446.4 19.8 631.3 4.3 672.7 60.9 851.3 41.1c64-7.2 121.9-20.8 172.7-37.9V.156H0V162.1z"/></svg>
    </section>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables.scss' as *;
.popular-dishes{
    margin-top: 130px;
    text-align: center;

    .cards-dishes{
        display: flex;
        gap: 33px;
        margin-top: 78px;
        margin-bottom: 54px;
        .card{
            width: 382px;

            .text-card{
                padding-top: 27px;
                display: flex;
                flex-direction: column;
                gap: 21px;

                .price-card{
                    color: $red;
                    font-size: 13px;

                    .dash{
                        color: $black;
                    }
                }
            }
        }
    }

    .button{
        margin: 0 auto;
    }

    .fusion-waves-opacity-candy{
        background-image: url(../assets/images/first-order-background-scaled.jpg);
        background-position: top;
        background-size: cover;
    }
}
</style>