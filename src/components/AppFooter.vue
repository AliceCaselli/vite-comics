<script>

export default {
    data() {
        return {

            images: [
                'footer-facebook.png',
                'footer-twitter.png',
                'footer-youtube.png',
                'footer-pinterest.png',
                'footer-periscope.png'
            ]
        };
    },
}

</script>

<template>
    <footer>
        <div id="container-footer">
            <button>SIGN-UP NOW!</button>

            <div id="icons-container">
                <span>FOLLOW US</span>
                <div id="icons">
                    <img src="" alt="">
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
footer {
    width: 100%;
    background-color: #303030;

    #container-footer {
        max-width: 1200px;
        margin-left: auto;
        margin-right: auto;

        display: flex;
        flex-direction: row;
        justify-content: space-between;
        padding: 30px 0;

        button {
            background-color: #303030;
            border: 2px solid #0282f9;
            color: white;
            font-weight: bold;
        }

        #icons-container {
            display: flex;
            flex-direction: row;

            span {
                color: #0282f9;
                font-weight: bold;
            }
        }
    }
}
</style>