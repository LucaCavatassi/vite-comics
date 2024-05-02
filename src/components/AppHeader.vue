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
            <img src="/public/dc-logo.png" alt="">
            <ul>
                <li v-for="linkName in linksNamesArray"> <a href="">{{ linkName }}</a></li>
            </ul>
        </header>
    </div>
</template>

<style scoped lang="scss">
    @use "../style/partials/variables" as *;

    header {
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

                a{
                    text-decoration: none;
                    color: inherit;
                }

                &:hover {
                    color: $primary-color;
                }
            }
        }

        img {
            width: 70px;
        }
    }

</style>