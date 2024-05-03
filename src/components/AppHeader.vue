<script>
    export default {
        data() {
            return {
                linksNamesArray: ["characters", "comics", "movies", "tv", "games", "collectibles", "videos", "fans", "news", "shop"]
            }
        }
    }
</script>

<template>
    <div>
        <header class="small-wrapper">
            <img src="/dc-logo.png" alt="">
            <ul>
                <li v-for="linkName in linksNamesArray"> <a href="">{{ linkName }}</a></li>
            </ul>
        </header>
    </div>
</template>

<style scoped lang="scss">
    @use "../style/partials/variables" as *;

    header {
        height: 100px;
        padding: 20px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin: 0 auto;

        ul {
            list-style: none;
            display: flex;
            gap: 10px;

            li {
                color: $footer-bottom-grey;
                text-transform: uppercase;
                font-weight: bold;
                font-size: 0.7rem;
                display: block;
                position: relative;

                a{
                    text-decoration: none;
                    color: inherit;
                }

                &:hover {
                    color: $primary-color;
                }

                &:after {
                    content: '';
                    position: absolute;
                    width: 100%;
                    transform: scaleX(0);
                    height: 3px; 
                    top: 53px;
                    left: 0;
                    background-color: $primary-color;
                    transition: transform 0.25s ease-out;
                }

                &:hover::after {
                    transform: scaleX(1); /* Scale the underline on hover */
                }
            }
        }

        img {
            width: 70px;
        }
    }


</style>