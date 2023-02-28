<script>
    export default {
        data() {
            return {
                footerLinks: [
                    {
                        label: 'DC COMICS',
                        links: [
                            {
                                label: 'Characters',
                                link: '#'
                            },
                            {
                                label: 'Comics',
                                link: '#'
                            },
                            {
                                label: 'Movies',
                                link: '#'
                            },
                            {
                                label: 'TV',
                                link: '#'
                            },
                            {
                                label: 'Games',
                                link: '#'
                            },
                            {
                                label: 'Videos',
                                link: '#'
                            },
                            {
                                label: 'News',
                                link: '#'
                            },
                        ]
                    },
                    {
                        label: 'SHOP',
                        links: [
                            {
                                label: 'Shop DC',
                                link: '#'
                            },
                            {
                                label: 'Shop DC Collectibles',
                                link: '#'
                            }
                        ]
                    },
                    {
                        label: 'DC',
                        links: [
                            {
                                label: 'Terms Of Use',
                                link: ''
                            },
                            {
                                label: 'Privacy Policy (New)',
                                link: '#'
                            },
                            {
                                label: 'Ad Choices',
                                link: '#'
                            },
                            {
                                label: 'Advertising',
                                link: '#'
                            },
                            {
                                label: 'Jobs',
                                link: '#'
                            },
                            {
                                label: 'Subscriptions',
                                link: '#'
                            },
                            {
                                label: 'Talent Whorkshops',
                                link: ''
                            },
                            {
                                label: 'CPSC Certificates',
                                link: '#'
                            },
                            {
                                label: 'Ratings',
                                link: '#'
                            },
                            {
                                label: 'Shop Help',
                                link: '#'
                            },
                            {
                                label: 'Contact US',
                                link: '#'
                            }
                        ]
                    },
                    {
                        label: 'SITES',
                        links: [
                            {
                                label: 'DC',
                                link: '#'
                            },
                            {
                                label: 'MAD Magazine',
                                link: '#'
                            },
                            {
                                label: 'DC Kids',
                                link: '#'
                            },
                            {
                                label: 'DC Universe',
                                link: '#'
                            },
                            {
                                label: 'DC Power Visa',
                                link: '#'
                            },
                        ]
                    }
                ],
                footerCards: [
                    {
                        label: 'DIGITAL COMICS',
                        link: '#',
                        img: 'buy-comics-digital-comics.png'
                    },
                    {
                        label: 'DC MERCHANDISE',
                        link: '#',
                        img: 'buy-comics-merchandise.png'
                    },
                    {
                        label: 'SUBSCRIPTION',
                        link: '#',
                        img: 'buy-comics-subscriptions.png'
                    },
                    {
                        label: 'COMIC SHOP LOCATORS',
                        link: '#',
                        img: 'buy-comics-shop-locator.png'
                    },
                    {
                        label: 'DC POWER VISA',
                        link: '#',
                        img: 'buy-dc-power-visa.svg'
                    }
                ],
                socialLinks: [
                    {
                        img: 'footer-facebook.png',
                        link: '#'
                    },
                    {
                        img: 'footer-twitter.png',
                        link: '#'
                    },
                    {
                        img: 'footer-youtube.png',
                        link: '#'
                    },
                    {
                        img: 'footer-pinterest.png',
                        link: '#'
                    },
                    {
                        img: 'footer-periscope.png',
                        link: '#'
                    }
                ]
            }
        }
    }
</script>

<template>
    <div class="blueBanner">
        <div class="container">
            <div v-for="card in footerCards" :key="card.img" class="card">
                <img :src="'./src/img/' + card.img" alt="">
                <a :href="card.link"><h5>{{ card.label }}</h5></a>
            </div>
        </div>
    </div>
    <footer>
        <div class="container">
            <div class="footerLinks">
                <div v-for="section in footerLinks" :key="section.label">
                    <h2>{{section.label}}</h2>
                    <ul>
                        <li v-for="item in section.links">
                            <h3><a :href="item.link">{{item.label}}</a></h3>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="footerImg">
            </div>
        </div>
        <div class="socialFooter">
            <div class="container">
                <a href="#">
                    <button>
                        <h3>SIGN-UP NOW!</h3> 
                    </button>
                </a>
                <div class="followUs">
                    <h4 class="blue">FOLLOW US</h4>
                    <div v-for="social in socialLinks">
                        <a href="social.link"><img :src="'./src/img/' + social.img" alt=""></a>
                    </div>
                </div> 
            </div>
        </div>
    </footer>

</template>

<style lang="scss" scoped>
    .blueBanner {
        background-color: rgb(60, 130, 240);
        .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            color: white;
        }
        
        .card {
            display: flex;
            align-items: center;
            white-space: nowrap;
        }

        img {
            height: 50px;
            margin: 1rem;
        }
    }


    

    footer {
        color: white;
        width: 100%;
        background-image: url(../img/footer-bg.jpg);
        background-size: contain;
        display: flex;
        flex-wrap: wrap;
    }
    
    .container {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
    }
    
    .footerLinks {
        width: 40%;
        height: 360px;
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;
        gap: 10px;

        li {
            margin: 0;
            padding: 0;
        }
    }
    


    .footerImg {
        width: 60%;
        align-self: stretch;
        display: flex;
        height: 360px;
        background-image: url(../img/dc-logo-bg.png);
        background-repeat: no-repeat;
        background-position: right;
        background-size: 70%;
    }

    .socialFooter {
        width: 100%;
        background-color: rgb(48, 48, 48);
    }

    button {
        padding: 10px;
        margin: 1rem 0;
        background-color: inherit;
        border: 2px solid rgb(60, 130, 240);
        color: white;
        cursor: pointer;
        filter: brightness(100%);
        transition: all .1s linear;
    }

    button:hover {
        filter: brightness(110%);
    }

    .followUs {
        display: flex;
        align-items: center;
        gap: 1rem;

        img {
            height: 30px;
            aspect-ratio: 1 / 1;
        }
    }
</style>
