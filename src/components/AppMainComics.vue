<script>

export default {

    name: 'AppMainComics',
    data() {
        return {};
    },

    props: {
        thumb: String,
        price: String,
        series: String,
        type: String,
    }
};
</script>

<template>
    <div class="comic-card">

        <div class="img-comics">
            <img :src="thumb" alt="image">
        </div>
        <div class="text">
            <span class="price">{{ price }}</span>
            <span class="series">{{ series }}</span>
            <span>{{ type }}</span>

        </div>

    </div>
</template>

<style lang="scss" scoped>
.comic-card {
    display: flex;
    flex-flow: column;
    align-items: center;


    width: calc(100% / 6 - 20px);


    .img-comics {

        width: 100%;

        height: 163px;
        overflow: hidden;


        img {
            width: 100%;
        }
    }

    .text {
        display: flex;
        flex-direction: column;
        align-items: center;
        padding-top: 20px;

        .price {
            font-size: 0.9em;
        }

        .series {
            font-weight: bold;
            font-size: 1.1em;
            text-align: center;
        }
    }
}
</style>