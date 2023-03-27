<script>


export default {


    data() {
        return {

        }
    },

    props: {
        img: String,
        title: String,
    },




}


</script>

<template>
    <div id="card">
        <img :src="img" alt="comics-card-image">
        <div id="card-title">
            {{ title.toUpperCase() }}
        </div>


    </div>
</template>






<style lang="scss" scoped>

#card {
    display: flex;
    flex-flow: column nowrap;
    width: calc(100% / 6 - (10px));
    height: 300px;

    img {
        object-fit: cover;
        object-position: top;
        overflow: hidden;

        &:hover {
            cursor: pointer;
        }
    }

    #card-title {
        width: 100%;
        height: 100px;
        padding: 20px 0;
    }
}

</style>






