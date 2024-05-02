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
                <div class="all-links">
                    <ul v-for="(curElem, index) in allLinks">
                        <span>{{ curElem.name }}</span>
                        <li v-for="elem in allLinks[index].links"><a href="">{{ elem }}</a></li>
                    </ul>
                </div>
                <img :src="getImagePath(dcLogo)" alt="">
            </div>
    </footer>
</template>

<style scoped lang="scss">
    @use "../style/partials/variables" as *;

    footer{
        background-image: url(/src/assets/img/footer-bg.jpg);
        background-repeat: no-repeat;
        overflow: hidden;

        .footer-bottom{
            padding: 30px 0;
            margin: 0 auto;
            color: white;
            display: flex;
            justify-content: space-between;
            position: relative;
            height: 300px;
            ul {
                list-style: none;
            }
        }
    }

    img {
        height: 150%;
        position: absolute;
        top: -30%;
        right: 0;
    }

    .all-links {
        display: flex;
        gap: 10px;
    }

    a{
        text-decoration: none;
        color: $main-grey;
        font-size: 0.6rem;
    }

    span {
        text-transform: uppercase;
        font-weight: bold;
    }

    

</style>