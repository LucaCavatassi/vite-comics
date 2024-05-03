<script>
    export default {
        props: {
            cardThumb: String,
            cardPrice: Number,
            cardSeries: String,
            cardType: String,
        },

        data() {
            return {
            }
        }
    }
</script>

<template>
    <div>
        <div class="img-square">
            <img :src="cardThumb" :alt="cardSeries">
        </div>
        <span> {{ cardSeries }} </span>
    </div>
</template>

<style scoped lang="scss">
    @use "../style/partials/variables" as *;

    div {
        display: flex;
        flex-direction: column;

        .img-square{
            img {
                max-width: 100%;
                aspect-ratio: 1;
                object-fit: cover;
                object-position: top;
            }
        }
        span {
            padding-top: 5px;
            color: white;
            font-size: 0.6rem;
            text-transform: uppercase;
        }
    }
</style>