<script>
export default {
    data() {
        return {
            links: [
                'Home',
                'Order Online',
                'About',
                'News',
                'Contact us',
                'Shopping'
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
                    </button>
                </div>
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
        position: relative;
    }

    .sidebar{
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding-top: 68px;

        .sidebar-links{
            display: flex;
            gap: 14px;

            .active{
                color: $yellow;
            }
        }
    }

    .hero-text{
        display: flex;
        flex-direction: column;
        justify-content: center;
        font-weight: bold;
        height: 90%;

        .text-small{
            font-size: 43px;
        }

        .text-big{
            font-size: 63px;
            .text-yellow{
                color: $yellow;
            }
        }

        .button{
            background-color: $red;
            color: $white;
            width: max-content;
            border: 0;
            border-radius: 20px;
            padding: 10px 27px;
            margin-top: 49px;
        }

    }
}

</style>