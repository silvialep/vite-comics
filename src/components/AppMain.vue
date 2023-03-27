<script>
export default {
    data() {
        return {
            message: '--> Content goes here <--'
        }
    },
}

</script>

<template>
    <div id="jumbotron">
        <img src="/img/jumbotron.jpg" alt="">
    </div>
    <div id="container">
        <h2>
            {{ message }}

        </h2>

    </div>
</template>


<style lang="scss" scoped>

@use "../scss/variables" as *;

#jumbotron {
    width: 100%;
    height: 400px;

    img {
        width: 100%;
        height: 100%;
        overflow: hidden;
        object-fit: cover;
        object-position: top;

    }
}

#container {
    height: 100px;
    padding: 30px;

    h2 {
        text-align: center;
    }
}

</style>
