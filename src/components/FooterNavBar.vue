<script>
export default {
    data() {
        return {
            socialIcons: [
                '../../public/footer-facebook.png',
                '../../public/footer-twitter.png',
                '../../public/footer-youtube.png',
                '../../public/footer-pinterest.png',
                '../../public/footer-periscope.png',
            ]

        }
    },
}

</script>

<template>
    <div id="container">
        <div id="navbar-container">
            <div id="footer-button">
                <button>SIGN-UP NOW!</button>
            </div>

            <div id="footer-icons">
                <h3>FOLLOW US</h3>
                <img v-for="icon in socialIcons" :src="icon" alt="social icon">

            </div>

        </div>

    </div>

    
</template>


<style lang="scss" scoped>

@use "../scss/variables" as *;


#container {
    width: 100%;
    height: 100px;
    background-color: rgb(48, 48, 48);
}

#navbar-container {
    @include mainContainer();

    #footer-button {
        display: flex;
        align-items: center;

        button {
            padding: 10px;
            border: 2px solid rgb(2, 130, 249);
        }
    }

    #footer-icons {
        display: flex;
        flex-flow: row;
        align-items: center;
        gap: 20px;
        height: 100%;

        h3 {
            width: 50%;
            font-size: 1.2rem;
            color: rgb(2, 130, 249);
            padding-right: 20px;
        }

        img {
            height: 40%;
            object-fit: contain;
        }
    }
}
 
</style>
