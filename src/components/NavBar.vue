<script>
export default {
    data() {
        return {

        }
    },
}

</script>

<template>
    <div id="container">
        <div id="nav-container">
                <div id="left-nav">
                    <img src="../../public/dc-logo.png" alt="main logo">
                </div>
                <div id="right-nav">
                    <ul>
                        <li v-for="link in headerlinks"> {{ link.toUpperCase() }} </li>
                    </ul>
                </div>
    
            </div>

    </div>
    
</template>


<style lang="scss" scoped>
 #container {
    width: 100%;
    height: 80px;
    background-color: white;
 }

 #nav-container {
    display: flex;
    justify-content: space-between;
    max-width: 1200px;
    height: 100%;
    padding: 10px;
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
