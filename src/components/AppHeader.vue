<script>

import NavBar from "./NavBar.vue";

export default {
    data() {
        return {
            links: [
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
        NavBar,
    },
}

</script>

<template>
    <NavBar>
        

    </NavBar>
</template>


<style lang="scss" scoped>



</style>
