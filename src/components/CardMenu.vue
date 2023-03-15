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
        }
    }
}
</script>

<template>
    <div class="card">
        <img class="img-card" :src="imageCard" :alt="textCard">
        <div class="text-card">
            {{ textCard }}
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables.scss' as *;
.card{
    position: relative;

    .img-card{
        filter: brightness(70%);
    }

    .text-card{
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        color: $white;
        font-weight: bold;
        text-transform: uppercase;
    }
}
</style>