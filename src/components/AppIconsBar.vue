<script>

export default {
    data() {
        return {
            icons: [
                {
                    image: '/img/buy-comics-digital-comics.png',
                    name: 'digital comics',
                },
                {
                    image: '/img/buy-comics-merchandise.png',
                    name: 'dc merchandise',
                },
                {
                    image: '/img/buy-comics-subscriptions.png',
                    name: 'subscription',
                },
                {
                    image: '/img/buy-comics-shop-locator.png',
                    name: 'comic shop locator',
                },
                {
                    image: '/img/buy-dc-power-visa.svg',
                    name: 'dc power visa',
                },
            ]
        }
    },

    components: {

    },



}

</script>

<template>
    <div id="container">
        <div id="icons-container">
            <div id="single-icon" v-for="(icon, index) in icons">
                <img :src="icon.image" alt="shop icons">
                <span> {{ icon.name.toUpperCase() }} </span>

            </div>

        </div>
        
    </div>
</template>

<style lang="scss" scoped>

@use "../scss/variables" as *;


#container {
    width: 100%;
    height: 150px;
    background-color: rgb(2, 130, 249);


    #icons-container {

        @include mainContainer();

        flex-flow: row nowrap;
        padding: 0 40px;

        #single-icon {
            display: flex;
            align-items: center;
            height: 100%;

            img {
                height: 3em;
            }
            
            &:last-child img {
                height: 2.5em;
            }

            span {
                padding: 0 10px;

                &:hover {
                    cursor: pointer;
                    text-shadow: 2px 2px 5px rgb(231, 233, 235);
                }
            }

        }
    
    }
}


</style>