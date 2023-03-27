<script>

import AppCard from './AppCard.vue';

export default {
    data() {
        return {
            cards: [
                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
                }
            ]
        }
    },

    components: {
        AppCard
    }
}

</script>

<template>
    <div id="jumbotron">
        <img src="/img/jumbotron.jpg" alt="">
    </div>
    <div id="container">
        <div id="comics-tag">
            <h3>Current Series</h3>
        </div>
        <AppCard v-for="(card, index) in cards" :img="card.thumb" :title="card.series"></AppCard>

        <div id="button-container">
            <button>LOAD MORE</button>
        </div>
    </div>
</template>


<style lang="scss" scoped>

@use "../scss/variables" as *;

#jumbotron {
    width: 100%;
    height: 400px;

    img {
        width: 100%;
        height: 100%;
        overflow: hidden;
        object-fit: cover;
        object-position: top;
    }
}


#container {
    @include mainContainer();
    position: relative;
    flex-flow: row wrap;
    justify-content: center;
    gap: 10px;
    padding: 100px 0 20px;


    #button-container {
        padding-top: 40px;

        button {
            padding: 10px 50px;
            background-color: rgb(2, 130, 249);
            border: none;

            &:hover {
                cursor: pointer;
            }
        }
    }

    #comics-tag {
        position: absolute;
        top: -3%;
        left: 0;
        z-index: 1;
        width: 250px;
        height: 60px;
        text-align: center;
        background-color: rgb(2, 130, 249);

        h3 {
            display: inline;
            font-size: 1.5rem;
            text-transform: uppercase;
            line-height: 60px;
            vertical-align: center;
        }
    }
}


</style>
