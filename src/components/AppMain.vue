<script>
import AppMainComics from './AppMainComics.vue';
export default {

    name: 'AppMain',
    data() {
        return {

            comics: [
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
        };
    },

    components: {
        AppMainComics,
    }
};
</script>

<template>
    <div id="container-main">
        <div id="jumbo">
        </div>
    </div>
    <div id="container-comics">
        <div id="current-series">CURRENT SERIES</div>

        <AppMainComics v-for="comic in comics" :thumb="comic.thumb" :price="comic.price" :series="comic.series"
            :type="comic.type"></AppMainComics>
    </div>
    <div class="btn">

        <button class="btn-load">LOAD MORE</button>
    </div>
</template>

<style lang="scss" scoped>
#container-main {

    #jumbo {

        height: 400px;
        background-image: url(/img/jumbotron.jpg);
        background-repeat: no-repeat;
        background-size: cover;

    }




}

#container-comics {
    max-width: 1100px;
    margin: 0 auto;

    display: flex;
    flex-flow: row wrap;
    justify-content: space-between;
    align-content: space-between;

    padding: 50px 0;

    height: 750px;

    position: relative;

    #current-series {

        position: absolute;
        top: -30px;
        left: -20px;

        display: flex;
        justify-content: center;
        align-items: center;
        background-color: #0282f9;
        font-weight: bold;

        font-size: 1.3em;
        height: 60px;
        width: 200px;
    }

}

.btn {
    display: flex;
    justify-content: center;
    padding: 30px 0;

    .btn-load {
        color: white;
        font-weight: bold;
        padding: 10px 50px;
        background-color: #0282f9;
        border: 1px solid transparent;
    }
}
</style>