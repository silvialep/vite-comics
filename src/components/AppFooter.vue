<script>

import FooterNavBar from "../components/FooterNavBar.vue";


export default {
    data() {
        return {
            dcComics: [
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

            shop: [
                'Shop DC',
                'Shop DC Collectibles'
            ],

            dcLinks: [
                'Terms Of Use',
                'Privacy Policy (New)',
                'Ad Choices',
                'Advertising',
                'Jobs',
                'Subscriptions',
                'Talent Workshops',
                'CPSC Certificates',
                'Ratings',
                'Shop Help',
                'Contact Us'
            ],

            sites: [
                'DC',
                'MAD Magazine',
                'DC Kids',
                'DC Universe',
                'DC Power Visa'
            ]
            
        }
    },
    
    components: {
        FooterNavBar,
    },
}

</script>

<template>
    
    <div id="footer-wallpaper">
        <div id="footer-container">
            <div id="footer-lists">
                <ul>
                    <li><h3> DC COMICS </h3></li>
                    <li v-for="item in dcComics"> {{ item }} </li>
                </ul>
                <ul>
                    <li><h3> SHOP </h3></li>
                    <li v-for="item in shop"> {{ item }} </li>
                </ul>
                <ul>
                    <li><h3> DC COMICS </h3></li>
                    <li v-for="item in dcLinks"> {{ item }} </li>
                </ul>
                <ul>
                    <li><h3> DC COMICS </h3></li>
                    <li v-for="item in sites"> {{ item }} </li>
                </ul>
            </div>

            <div id="footer-logo">
                <img src="/dc-logo-bg.png" alt="logo footer">
            </div>
            
        </div>
        
    </div>

    <FooterNavBar>

    </FooterNavBar>
    
</template>


<style lang="scss" scoped>

@use "../scss/variables" as *;

#footer-wallpaper {
    width: 100%;
    height: 350px;
    background-image: url(/footer-bg.jpg);
    background-size: cover;
}

#footer-container {
    @include mainContainer();
    padding: 0;
    
    ul {
        // font-size: 0.6rem;
        list-style-type: none;
        color: rgb(149, 149, 149);
        padding: 20px 0 0;
        

        h3 {
            color: white;
        }
    }

    #footer-logo {
        width: 50%;
        height: 100%;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: center;
            overflow: hidden;
        }
    }
}

#footer-lists {
    display: flex;
    flex-flow: column wrap;
    gap: 15px;
}





</style>
