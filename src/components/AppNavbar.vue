<script>

export default {
    data() {
        return {

            links: [
                'characters',
                'comics',
                'movies',
                'tv',
                'games',
                'collectibles',
                'videos',
                'fans',
                'news',
                'shop'

            ],

            activeIndex: -1,
        };


    },

    methods: {
        classActive(clickIndex) {

            this.activeIndex = clickIndex;
        }

    }
};

</script>

<template>
    <div id="navbar">

        <div id="container-navbar">
            <img src="/img/dc-logo.png" alt="">

            <nav>

                <ul id="link-list">
                    <li v-for="(link, index) in links" @click="classActive(index)"
                        :class="index == activeIndex ? 'active' : ''">{{ link }}</li>
                </ul>
            </nav>
        </div>
    </div>
</template>

<style lang="scss" scoped>
#navbar {
    width: 100%;
    background-color: white;
}


#container-navbar {
    display: flex;
    align-items: center;
    justify-content: space-around;

    max-width: 1200px;
    margin-left: auto;
    margin-right: auto;
    padding: 20px;
}



#link-list {
    display: flex;
    flex-flow: row;
    gap: 30px;
    list-style-type: none;

    .active {

        color: #0282f9;
        border-bottom: 4px solid #0282f9;
    }


    li {
        text-transform: uppercase;
        cursor: pointer;
        color: black;
        font-weight: bold;

        &:hover {
            color: #0282f9;
        }


    }
}
</style>