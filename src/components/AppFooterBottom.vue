<script>
    export default {
        data() {
        return {
            dcLogo: "dc-logo-bg.png",

            allLinks: [
                    {
                        name: "dc comics",
                        links: ["Characters", "Comics", "Movies", "Tv", "Games", "Videos", "News"]
                    },

                    {
                        name: "shop",
                        links: ["Shop DC", "Shop DC Collectibles"]
                    },

                    {
                        name: "dc",
                        links: ["Terms Of Use", "Privacy Policy (New)", "Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshops", "CPSC Certificates", "Ratings", "Shop Help", "Contact Us"]
                    },

                    {
                        name: "sites",
                        links: ["DC", "MAD Magazine", "DC Kids", "DC Univers", "DC Power Visa"]
                    }
                ]
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
    <footer>
            <div class="footer-bottom small-wrapper" >
                Footer Left
                <img :src="getImagePath(dcLogo)" alt="">
            </div>
    </footer>
</template>

<style scoped lang="scss">
    footer{
        background-image: url(/src/assets/img/footer-bg.jpg);
        background-repeat: no-repeat;
        overflow: hidden;

        .footer-bottom{
            margin: 0 auto;
            color: white;
            display: flex;
            justify-content: space-between;
            position: relative;
            height: 300px;
        }
    }

    img {
        height: 150%;
        position: absolute;
        top: -30%;
        right: 0;
    }

</style>