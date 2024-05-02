<script>
    export default {
        data() {
            return {
                logos: ["footer-facebook.png", "footer-periscope.png", "footer-pinterest.png", "footer-twitter.png", "footer-youtube.png"]
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
    <div class="container">
        <main class="small-wrapper">
            <div> 
                <span class="button"> <a href="">SIGN-UP NOW!</a></span>
                <div class="socials">
                    <span>FOLLOW US</span>
                    <ul v-for="logo in logos">
                        <li><a href=""><img :src="getImagePath(logo)" alt=""></a></li>
                    </ul>
                </div>
            </div>
        </main>
    </div>
</template>

<style scoped lang="scss">
    @use "../style/partials/variables" as *;

    .container {
        display: flex;
        justify-content: center;
        background-color: $footer-bottom-grey;
        div {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
            color: white;
            font-weight: bolder;

            .button {
                border: 2px solid $primary-color;
                padding: 10px;
                a{
                    text-decoration: none;
                    color: inherit;
                }
            }

            .socials {
                span{
                    color: $primary-color;
                    padding-right: 20px;
                }
                ul {
                    list-style: none;
                    padding: 0 5px;
                }
            }
        }
    }
</style>