<script>

import FooterNavBar from "../components/FooterNavBar.vue";


export default {
    data() {
        return {
            comicsLinks: [
                {
                    title: 'Dc Comics' ,
                    links: [
                        'Characters',
                        'Comics',
                        'Movies',
                        'TV',
                        'Games',
                        'Videos',
                        'News',
                    ]
                },
                {
                    title: 'Shop',
                    links: [
                        'Shop DC',
                        'Shop DC Collectibles'
                    ]
                },
                {
                    title: 'DC',
                    links: [
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
                    ]
                },
                {
                    title: 'Sites',
                    links: [
                        'DC',
                        'MAD Magazine',
                        'DC Kids',
                        'DC Universe',
                        'DC Power Visa'
                    ]
                }
                

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
                <ul v-for="group in comicsLinks">
                    <li :class="'link-title'"> {{ group.title.toUpperCase() }} </li>
                    <li v-for="link in group.links"> <a href="#"> {{ link }} </a></li>
                </ul>
                
            </div>

            <div id="footer-logo">
                <img src="/img/dc-logo-bg.png" alt="logo footer">
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
    background-image: url(/img/footer-bg.jpg);
    background-size: cover;
}

#footer-container {
    @include mainContainer();
    padding: 0;
    
    ul {
        // font-size: 0.6rem;
        list-style-type: none;
        

        .link-title {
            padding: 10px 0;
            font-weight: bold;
            font-size: 1rem;
            color: white;
        }

        a {
            text-decoration: none;
            color: rgb(149, 149, 149);
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


    #footer-lists {
        display: flex;
        flex-flow: column wrap;
        gap: 20px;
        padding-top: 20px;
    }
}






</style>
