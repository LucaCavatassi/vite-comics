<script>
import ComicCard from "./ComicCard.vue"

export default {
    components: {
        ComicCard,
    },

    data() {
        return {
            allComics: [
                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book",
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book",
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel",
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel",
                },
            ],
        }
    }
}
</script>

<template>
    <div class="container">
        <main class="small-wrapper">
            <span>CURRENT SERIES</span>
            <div class="row"> 
                <div class="col" v-for="comic in allComics">
                    <ComicCard 
                    :cardThumb = "comic.thumb"
                    :cardSeries="comic.series"
                    />
                </div>
            </div>
            <div class="button">
                <button>LOAD MORE</button>
            </div>
        </main>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;

.container {
    display: flex;
    justify-content: center;
    background-color: $main-black;
    main {
        position: relative;

        span {
            color: white;
            font-weight: bold;
            background-color: $primary-color;
            padding: 10px;
            position: absolute;
            top: -20px;
            left: -10px;
            
        }

        .row {
            margin-top: 30px;
            padding-top: 10px;
            display: flex;
            justify-content: space-between;
            align-items: stretch;
            flex-wrap: wrap;
            gap: 10px;
    
            .col{
                width: calc(100% / 6 - 25px);
            }
        }

        .button{
            margin: 30px 20px;
            button {
                margin: 0 auto;
                padding: 5px 20px;
                display: block;
                font-family: sans-serif;
                background-color: $primary-color;
                border: none;
                color: white;
                font-weight: bold;
            }
        }
    }
}
</style>