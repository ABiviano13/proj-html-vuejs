<script>
export default {

}
</script>

<template>
    <section class="news">
        <div class="container">
            <div class="row-button">
                <button class="button">
                    Read more news
                    <i class="fa-solid fa-circle-arrow-right"></i>
                </button>
            </div>
            <h1 class="title">
                Latest News
            </h1>

            <div class="cards-news">
                <div class="card">
                    <img class="img-card" src="../assets/images/pancake-burger.jpg" alt="">
                    <div class="text-card">
                        <h2 class="title-card">
                            <span class="uppercase">New</span>: The Pancake Burger
                        </h2>
                        <div class="text-xsmall">
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi sodales <br>
                            ipsum vel elementum vehicula. Suspendisse sit amet aliquet ex. <br>
                            Pellentesque commodo tortor vel mi
                        </div>
                    </div>
                </div>
                <div class="card">
                    <img class="img-card" src="../assets/images/new-milkshake-menu.jpg" alt="">
                    <div class="text-card">
                        <h2 class="title-card">
                            New Milkshake Menu
                        </h2>
                        <div class="text-xsmall">
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi sodales <br>
                            ipsum vel elementum vehicula. Suspendisse sit amet aliquet ex. <br>
                            Pellentesque commodo tortor vel mi
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>

.news {
    margin-bottom: 184px;
    .row-button{
        display: flex;
        justify-content: end;
    }

    .cards-news {
        display: flex;
        .card{
            text-align: center;
            .img-card{
                height: 437px;
                margin-bottom: 43px;
            }

            .uppercase{
                text-transform: uppercase;
            }

            .text-xsmall{
                font-size: 13px;
                margin-top: 23px;
                line-height: 2;
            }
        }
    }

}

</style>