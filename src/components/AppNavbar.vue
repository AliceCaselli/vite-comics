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
        };
    },
};

</script>

<template>
    <div id="navbar">

        <div id="container-navbar">
            <img src="/img/dc-logo.png" alt="">

            <nav>

                <ul id="link-list">
                    <li v-for="link in links">{{ link }}</li>
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


    li {
        text-transform: uppercase;
        cursor: pointer;
        color: black;
        font-weight: bold;
        border-bottom: 4px solid #0282f9;

        &:hover {
            color: #0282f9;
        }
    }
}
</style>