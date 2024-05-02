<script>
    export default {
        data() {
        return {
            blueFoot: [
                {
                    img: "buy-comics-digital-comics.png", 
                    text: "digital comics",
                },

                {
                    img: "buy-comics-merchandise.png", 
                    text: "dc merchandise",
                },

                {
                    img: "buy-comics-subscriptions.png", 
                    text: "subscription",
                },

                {
                    img: "buy-comics-shop-locator.png", 
                    text: "comic shop locator",
                },

                {
                    img: "buy-dc-power-visa.svg", 
                    text: "dc power visa"
                },
            ],
        }
        },
        methods: {
            getImagePath (imageName) {
                return new URL(`../assets/img/${imageName}`, import.meta.url).href;
            }
        }
    }
</script>

<template>
    <footer class="footer-top">
        <div class="small-wrapper">
            <ul>
                <li v-for="curElem in blueFoot" >
                    <img :src="getImagePath(curElem.img)" alt="">
                    <span>{{ curElem.text }}</span>
                </li>
            </ul>
        </div>
    </footer class="footer-top">
</template>

<style scoped lang="scss">
    @use "../style/partials/variables.scss" as *;

    .footer-top {
        background-color: $secondary-color;
        display: flex;
        justify-content: center;
        padding: 20px 0;
        ul {
            list-style: none;
            display: flex;

            li {
                width: calc(100% / 3);
                display: flex;
                align-items: center;
                justify-content: center;
                gap: 10px;

                img {
                    height: 40%;
                }

                span {
                    text-transform: uppercase;
                    color: white;
                    font-size: 0.65rem;
                }
                
                &:last-child img {
                    max-width: 65px;
                }
            }
        }
    }
</style>