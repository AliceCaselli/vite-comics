<script>

export default {
    data() {
        return {

            cards: [
                {
                    img: '/img/buy-comics-digital-comics.png',
                    text: 'DIGITAL COMICS'
                },

                {
                    img: '/img/buy-comics-merchandise.png',
                    text: 'DC MERCHANDISE'
                },

                {
                    img: '/img/buy-comics-subscriptions.png',
                    text: 'SUBSCRIPTION'
                },

                {
                    img: '/img/buy-comics-shop-locator.png',
                    text: 'COMIC SHOP LOCATOR'
                },

                {
                    img: '/img/buy-dc-power-visa.svg',
                    text: 'DC POWER VISA'
                }

            ]
        };
    },
}

</script>

<template>
    <header>

        <div id="container-header">

            <a v-for="card in cards" id="card" href="#">
                <img :src="card.img" alt="">
                <span>{{ card.text }}</span>
            </a>
        </div>
    </header>
</template>

<style lang="scss" scoped>
header {
    width: 100%;
    background-color: #0282f9;

    #container-header {

        max-width: 1000px;
        margin-left: auto;
        margin-right: auto;

        padding: 30px 0;

        display: flex;
        flex-direction: row;
        justify-content: space-between;


        a {
            color: white;
            text-decoration: none;
            font-weight: bold;

            display: flex;
            flex-direction: row;
            align-items: center;
            gap: 10px;

            height: 45px;

            img {
                height: 100%;
            }

            span {
                font-size: 0.7em;
            }


        }
    }
}
</style>