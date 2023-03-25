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
    <div id="container">
        <h2>
            {{ message }}

        </h2>

    </div>
</template>


<style lang="scss" scoped>

@use "../scss/variables" as *;


#container {
    height: 250px;
    padding: 30px;

    h2 {
        text-align: center;
    }
}

</style>
