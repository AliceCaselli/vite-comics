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
                    img: '/img/buy-comics-subscription.png',
                    text: 'SUBSCRIPTION'
                },

                {
                    img: '/img/buy-comics-shop-locator.png',
                    text: 'COMIC SHOP LOCATOR'
                },

                {
                    img: '/img/buy-dc-power-visa',
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
            <div id="card">
                <img src="" alt="">
                <span v-for="card in cards">{{ card.text }}</span>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
header {
    width: 100%;
    height: 150px;
    background-color: #0282f9;

    #container-header {

        max-width: 1000px;
        margin-left: auto;
        margin-right: auto;
    }
}
</style>