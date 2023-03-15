<script>

export default {
    data() {
        return {
            listIndexFooter: [
                {
                    title: 'Order Online',
                    listItemIndex: [
                        'Appetizers',
                        'Burgers',
                        'Pizza',
                        'Fries',
                        'Sides',
                        'Desserts',
                        'Beverages',
                        'Specials'
                    ]
                },
                {
                    title: 'Navigate',
                    listItemIndex: [
                        'Home',
                        'Alternate Home',
                        'Menu',
                        'About',
                        'News',
                        'Contact Us',
                        'Cart'
                    ]
                },
                {
                    title: 'Information',
                    listItemIndex: [
                        'My account',
                        'Terms Of Service',
                        'Privacy Police',
                    ],
                    app: {
                        srcAppleStore: 'src/assets/images/app-store-badge.png',
                        srcPlayStore: 'src/assets/images/play-store-badge.png'
                    }
                },
                {
                    title: 'Opening Hours',
                    listItemIndex: [
                        'Mon - 10AM to 11PM',
                        'Tue - 10AM to 11PM',
                        'Wed - 10AM to 11PM',
                        'Thur - 10AM to 11PM',
                        'Fri - 10AM to 11PM',
                        'Sat - 10AM to 1AM',
                        'Sun - 11AM to 10PM',
                    ]
                },
                {
                    title: 'Voucher',
                    couponSrc: 'src/assets/images/footer-coupon.png',
                    textOne: 'Just Use The Code',
                    code: 'Firstorder',
                    textTwo: 'At Checkout'
                }
            ]
        }
    }
}

</script>

<template>

    <footer class="main-footer">
        <div class="container-footer">

            <ul class="list-link-index" v-for="(list, i) in listIndexFooter" :key="i">
                <div class="title-list">
                    {{list.title}}
                </div>
                <li class="listIndex" v-for="listItem in list.listItemIndex">
                    {{listItem}}
                </li>
                <li class="app" v-if="i == 2">
                    <img :src="list.app.srcAppleStore" alt="">
                    <img :src="list.app.srcPlayStore" alt="">
                </li>

                <li v-if="i == 4">
                    <img class="img-coupon" :src="list.couponSrc" alt="">
                    <div class="text-coupon">
                        {{ list.textOne }}
                        <div class="code">
                            {{ list.code }}
                        </div>
                        {{ list.textTwo }}
                    </div>
                </li>
            </ul>

        </div>

        <div class="registration">
            <img src="../assets/images/takeout-logo.png" alt="logo">
            <h4 class="title">
                Stay in the loop
            </h4>
            <div class="text">
                Sign up to receive up to date news and offers directly in your inbox:
            </div>
            <input class="input-text" type="text" placeholder="you@email.com">
            <button class="button">
                Subscribe
            </button>
            <ul class="list-icon">
                <li class="icon">
                    <i class="fa-brands fa-facebook-f"></i>
                </li>
                <li class="icon">
                    <i class="fa-brands fa-twitter"></i>
                </li>
                <li class="icon">
                    <i class="fa-brands fa-instagram"></i>
                </li>
                <li class="icon">
                    <i class="fa-brands fa-linkedin"></i>
                </li>
                <li class="icon">
                    <i class="fa-solid fa-wifi"></i>
                </li>
                <li class="icon">
                    <i class="fa-regular fa-envelope"></i>
                </li>
            </ul>
            <div class="copyright">
                <i class="fa-regular fa-copyright"></i>
                <span class="yellow">
                    Copyright 2012 - 2020 | Avada theme by 
                </span> 
                Theme Fusion 
                <span class="yellow">
                    | All Right Reserved | Powered by
                </span>
                WordPress
            </div>
        </div>
    </footer>

</template>

<style lang="scss" scoped>
@use '../style/partials/variables.scss' as *;
.main-footer{
    background-image: url('../assets/images/footer-background-scaled.jpg');
    background-position: center;
    background-size: cover;
    color: $white;
    .container-footer{
        max-width: 1423px;
        padding-top: 137px;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;

        .list-link-index{
            line-height: 2;
            margin-bottom: 68px;

            .listIndex{
                &:hover{
                    color: $yellow;
                }
            }

            .title-list{
                text-transform: uppercase;
                text-align: center;
                margin-bottom: 34px;
            }

            .app{
                display: flex;
                flex-direction: column;
                gap: 10px;
                margin-top: 24px;

                img {
                    height: 52px;
                    border: 1px solid $white;
                    border-radius: 10px;
                }
            }

            .img-coupon{
                height: 150px;
            }

            .text-coupon{
                text-align: center;
                font-weight: bold;

                .code{
                    text-transform: uppercase;
                    color: $yellow;
                }
            }
        }
    }
    .registration{
        text-align: center;
        margin: 0 auto;
        line-height: 2;
        padding-bottom: 245px;

        .title{
            color: $yellow;
            margin-top: 47px;
        }

        .input-text{
            border-radius: 20px;
            border: 0;
            padding: 5px;
            width: 700px;
            height: 45px;
        }

        .button{
            position: relative;
            left: 50%;
            transform: translate(-50%);
            margin-top: 31px;
            margin-bottom: 53px;
            width: 700px;
            justify-content: center;
        }

        .list-icon{
            margin: 0 auto;
            color: $white;
            display: flex;
            justify-content: center;
            gap: 20px;
            font-size: 16px;
        }

        .copyright {
            .yellow{
                color: $yellow;
                font-size: 13px;
            }
        }
    }
}
</style>