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
        <img :src="cardThumb" :alt="cardSeries">
        <span> {{ cardSeries }} </span>
    </div>
</template>

<style scoped lang="scss">
    @use "../style/partials/variables" as *;

    div {
        display: flex;
        flex-direction: column;
        span {
            color: white;
        }
        img {
            max-width: 100%;
        }
    }
</style>