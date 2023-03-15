<script>
export default {
    props: {
        imageCard: {
            type: String,
            required: true
        },
        textCard: {
            type: String,
            required: true
        },
        priceCard: {
            type: String,
            required: true
        }
    }
}
</script>

<template>
    <div class="card">
        <figure>
            <img class="card-img"  :src="imageCard" :alt="textCard">
        </figure>
        <div class="text-card">
            <h2>
                {{textCard}}
            </h2>
            <div class="price-card">
                {{priceCard}}
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables.scss' as *;
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

</style>