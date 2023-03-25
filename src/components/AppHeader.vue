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
            ]

        }
    },

    components: {
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
                    <li v-for="link in headerLinks"> {{ link.toUpperCase() }} </li>
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

    background-color: white;

    #left-nav {
        height: 100%;

        img {
            height: 100%;
        }
    }

    #right-nav {
        height: 100%;

        ul {
            display: flex;
            flex-flow: row nowrap;
            gap: 10px;
            align-items: center;
            height: 100%;
            color: rgb(82, 70, 70);
            list-style-type: none;
        }
    }
}
    



</style>
