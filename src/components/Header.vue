<script>

export default {
    data() {
        return {
            links: [
                'Home',
                'Order Online',
                'About',
                'News',
                'Contact us'
            ],
            services: [
                '24/7 Delivery',
                'Over 100 Dishes',
                'In app ordering',
                'Fast Delivery'
            ]
        }
    }
}
</script>

<template>

    <header class="main-header">
        <div class="hero">
            <div class="container">
                <div class="sidebar">
                    <figure class="logo">
                        <img src="../assets/images/takeout-logo.png" alt="logo-takeout">
                    </figure>
                    <ul class="sidebar-links">
                        <li class="link"
                        :class="i == 0 ? 'active' : ''"
                        v-for="(link,i) in links" :key="i"
                        >
                            {{ link }}             
                        </li>
                        <li class="link">
                            <i class="fa-solid fa-cart-shopping"></i>
                        </li>

                    </ul>
                </div>
                <div class="hero-text">
                    <div class="text-small">
                        Hungry?
                    </div>
                    <div class="text-big">
                        <div class="text-yellow">
                            Great Food
                        </div>
                        Delivered
                    </div>
                    <button class="button">
                        View our Menu
                        <i class="fa-solid fa-circle-arrow-right"></i>
                    </button>
                </div>
                <ul class="bar-services">
                    <li class="service"
                    v-for="service in services">
                        {{ service }}
                    </li>
                </ul>
            </div>
        </div>
    </header>

</template>

<style lang="scss">
@use '../style/partials/variables.scss' as *;

.main-header{
    background-image: url(../assets/images/home-background-hero-scaled.jpg);
    background-size: cover;
    background-position: center;
    width: 100%;
    height: 100vh;
    color: $white;

    .hero{
        height: 100%;
    }

    .sidebar{
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding-top: 68px;

        .sidebar-links{
            display: flex;
            gap: 46px;

            .active{
                color: $yellow;
            }

            .shopping-cart{
                width: 18px;
            }
        }
    }

    .hero-text{
        display: flex;
        flex-direction: column;
        justify-content: center;
        font-weight: bold;
        height: 85%;
        margin-bottom: -25px;

        .text-small{
            font-size: 40px;
        }

        .text-big{
            font-size: 65px;
            margin-bottom: 49px;
            .text-yellow{
                color: $yellow;
            }
        }

    }

    .bar-services{
        background-color: $white;
        color: $black;
        display: flex;
        justify-content: space-evenly;
        font-size: 10px;
        text-transform: uppercase;
        padding: 45px 0;
    }
}

</style>