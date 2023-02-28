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
                ]
            }
        }
    }
</script>

<template>
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
    </footer>
</template>

<style scoped>
    footer {
        color: white;
        width: 100%;
        background-image: url(../img/footer-bg.jpg);
        display: flex;
        flex-wrap: nowrap;
    }

    h2 {
        font-size: 1.5rem;
    }

    h3 {
        font-size: .8rem;
    }
    
    .container {
        display: flex;
        flex-direction: row;
    }
    
    .footerLinks {
        width: 40%;
        height: 410px;
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;
        gap: 1.5rem;
        
    }
    
    a {
        opacity: .6;
        filter: brightness(100%);
        transition: all .1s linear;
    }

    a:hover {
        opacity: .8;
        filter: brightness(110%);
    }

    .footerImg {
        width: 60%;
        align-self: stretch;
        display: flex;
        height: 430px;
        background-image: url(../img/dc-logo-bg.png);
        background-repeat: no-repeat;
        background-position: right;
        background-size: 70%;
    }
</style>
