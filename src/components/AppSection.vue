<script>

export default {
    data() {
        return {

            lists: [
                {
                    title: 'dc comics',
                    links: [
                        'characters',
                        'comics',
                        'movies',
                        'tv',
                        'games',
                        'videos',
                        'news'
                    ]
                },

                {
                    title: 'dc',
                    links: [
                        'term of use',
                        'privacy policy (new)',
                        'ad choises',
                        'advertising',
                        'jobs',
                        'subscriptions',
                        'talent workshop',
                        'CPSC certificates',
                        'ratings',
                        'shop help',
                        'contact us'
                    ]
                },

                {
                    title: 'sites',
                    links: [
                        'DC',
                        'MAD magazine',
                        'DC kids',
                        'DC universe',
                        'DC power visa',
                    ]
                },

                {
                    title: 'shop',
                    links: [
                        'shop DC',
                        'shop DC collectibles'
                    ]
                }

            ]
        };
    },
}

</script>

<template>
    <div id="section">
        <div id="container-section">

            <div id="list-container">
                <div v-for="list in lists" id="lists">
                    <ul>
                        <strong>{{ list.title }}</strong>
                        <li v-for="link in list.links">{{ link }}</li>
                    </ul>
                </div>
            </div>

            <div id="logo">
                <img src="/img/dc-logo-bg.png" alt="">
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
#section {
    height: 400px;
    background-image: url(/img/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    overflow: hidden;

    width: 100%;

    #container-section {
        display: flex;
        justify-content: space-between;

        max-width: 1200px;
        margin-left: auto;
        margin-right: auto;

        #list-container {
            width: 50%;
            display: flex;
            flex-flow: row wrap;
            align-items: flex-start;
            gap: 50px;
            padding-top: 10px;

            #lists {

                ul {
                    padding: 0;
                    list-style-type: none;
                    display: flex;
                    flex-direction: column;

                    strong {
                        text-transform: uppercase;
                        display: inline-block;
                        margin-bottom: 15px;
                    }

                    li {
                        text-transform: capitalize;
                        font-size: 0.9em;
                        color: rgb(168, 167, 167);
                    }


                }
            }
        }

        #logo {

            img {
                height: 600px;
            }

        }
    }
}
</style>