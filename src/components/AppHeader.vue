<script>


export default {
    data() {
        return {
            headerLinks: [
                'Characters',
                'Comics',
                'Movies',
                'TV',
                'Games',
                'Collectibles',
                'Videos',
                'Fans',
                'News',
                'shop',
            ],

            activeIndex: null,

        }
    },

    components: {
    },

    methods: {
        activeLink(index) {
            this.activeIndex = index;
        }
    },
}

</script>







<template>
    <nav id="container">
        <div id="nav-container">
            <div id="left-nav">
                <img src="../../dc-logo.png" alt="main logo">
            </div>
            <div id="right-nav">
                <ul>
                    <li v-for="link, index in headerLinks" @click="activeLink(index)" :class="activeIndex == index ? 'active' : ''"> {{ link.toUpperCase() }} </li>
                </ul>
            </div>

        </div>

    </nav>
</template>









<style lang="scss" scoped>

@use "../scss/variables" as *;

#container {
    width: 100%;
    height: 80px;
    background-color: white;
 }

 #nav-container {
    @include mainContainer();
    
    padding: 0;


    background-color: white;

    #left-nav {
        height: 100%;

        img {
            padding: 5px;
            height: 100%;
        }
    }

    #right-nav {
        height: 100%;

        ul {
            display: flex;
            flex-flow: row nowrap;
            gap: 20px;
            align-items: center;
            height: 100%;
            color: rgb(82, 70, 70);
            list-style-type: none;

            li {
                position: relative;
                display: flex;
                align-items: center;
                height: 100%;
                // border-bottom: 5px solid white;
                // border-top: 5px solid white;

                &:hover {
                    cursor: pointer;
                }

                &:hover:before{
                    content: '';

                    position: absolute;
                    bottom: 0;

                    width: 100%;
                    height: 5px;
                    background-color: rgb(2, 130, 249);

                }

            }
            .active {
                color: rgb(2, 130, 249);

                &::before {
                    content: '';

                    position: absolute;
                    bottom: 0;

                    width: 100%;
                    height: 5px;
                    background-color: rgb(2, 130, 249);
                }

                
                }
            }
        }
    }


    



</style>
