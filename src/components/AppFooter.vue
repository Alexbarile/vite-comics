<script>
export default {
    data() {
        return {
            icon: [
                {
                    label: 'buy-comics-digital-comics.png',
                    active: false,
                    description: 'DIGITAL COMICS'
                },
                {
                    label: 'buy-comics-merchandise.png',
                    active: true,
                    description: 'DC MERCHANDISE'
                },
                {
                    label: 'buy-comics-subscriptions.png',
                    active: false,
                    description: 'SUBSCRIPTION'
                },
                {
                    label: 'buy-comics-shop-locator.png',
                    active: false,
                    description: 'COMIC SHOP LOCATOR'
                },
                {
                    label: 'buy-dc-power-visa.svg',
                    active: false,
                    description: 'DC POWER VISA'
                },
            ],
            social: [
                {
                    logo: 'footer-facebook.png',
                },
                {
                    logo: 'footer-periscope.png',
                },
                {
                    logo: 'footer-pinterest.png',
                },
                {
                    logo: 'footer-twitter.png',
                },
                {
                    logo: 'footer-youtube.png',
                },
            ]
        }
    },

    // funzione per mostrare le icone nelle prima parte del footer

    methods: {
        getImagePath: function (img) {
            return `/img/${img}`
        }
    }
    
}
</script>

<template lang="">
    <footer>

        <!-- prima parte footer -->

        <div class="bg-blu">
            <div class="container">
               <div class="row">
                    <div class="col">
                        <ul>
                            <li v-for="(i, index) in icon" :key="i">
                                <a href="#">
                                    <img :src="getImagePath(i.label)" alt="logo">
                                    <!-- <img :src="`/img/${i.label}`" alt="logo"></img> -->
                                    <span>{{i.description}}</span>
                                </a>
                            </li>
                        </ul>
                    </div>
               </div>
            </div>
        </div>

        <!-- seconda parte footer -->

        <div class="jumbo">
            <div class="container">
                <div class="row">

                    <!-- link -->

                    <div class="col">
                        <div>
                            <h3>Dc comics</h3>
                            <ul>
                                <li><a href="#">Characters</a></li>
                                <li><a href="#">Comics</a></li>
                                <li><a href="#">Movies</a></li>
                                <li><a href="#">TV</a></li>
                                <li><a href="#">Games</a></li>
                                <li><a href="#">Videos</a></li>
                                <li><a href="#">News</a></li>
                            </ul>
                            <h3>Shop</h3>
                            <ul>
                                <li><a href="#">Shop DC</a></li>
                                <li><a href="#">Shop DC Collectibles</a></li>
                            </ul>
                        </div>
                        <div>
                            <h3>Dc</h3>
                            <ul>
                                <li><a href="#">Temos Of Use</a></li>
                                <li><a href="#">Privacy policy (New)</a></li>
                                <li><a href="#">Ad Choices</a></li>
                                <li><a href="#">Advertising</a></li>
                                <li><a href="#">Jobs</a></li>
                                <li><a href="#">Subscriptions</a></li>
                                <li><a href="#">Talent Workshops</a></li>
                                <li><a href="#">CPSC Cerrificates</a></li>
                                <li><a href="#">Ratings</a></li>
                                <li><a href="#">Shop Help</a></li>
                                <li><a href="#">Contact Us</a></li>
                            </ul>
                        </div>
                        <div>
                            <h3>Sites</h3>
                            <ul>
                                <li><a href="#">DC</a></li>
                                <li><a href="#">MAD Magazine</a></li>
                                <li><a href="#">DC Kids</a></li>
                                <li><a href="#">DC Universe</a></li>
                                <li><a href="#">DC Power Visa</a></li>
                            </ul>
                        </div>
                    </div>

                    <!-- logo grande -->

                    <div class="col">
                        <img src="/img/dc-logo-bg.png" alt="dc-logo">
                    </div>
                </div>
            </div>
        </div>

        <!-- terza parte footer -->

        <div class="social">
            <div class="container">
                <div class="row">

                    <!-- button -->

                    <div class="col">
                        <button><a href="#"> Sign-Up Now!</a></button>
                    </div>

                    <!-- loghi social -->

                    <div class="col">
                        <ul>
                            <h3>Follow Us</h3>
                            <ul>
                                <li v-for="(item, index) in social" :key="index">
                                    <a href="#"><img :src="getImagePath(item.logo)" alt="loghi-social"></a>
                                </li>
                            </ul>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

// prima parte footer

        .bg-blu{
            background-color: $blu;

            .row{

                ul{
                    @include space_between;
                }

                li{
                    @include space_between;
                    padding: 20px;
                }

                a{
                    color: $white;
                    font-weight: 300;
                    text-decoration: none;
                    @include center;

                   img{
                    width: 60px;
                    padding: 10px;
                   }

                   span{
                    font-size: 12px;
                   }
                }
            }
        }

// seconda parte footer

        .jumbo{
            background-image: url('../../public/img/footer-bg.jpg');
            background-size: cover;
            // non uscirà nulla perchè serve il contenuto

            .row{
                @include space_between;
            }

            .col{
                display: flex;

                div{
                    margin-right: 30px;
                }
            }

            h3{
                @include upbold;
                font-size: 20px;
                color: $white;
                padding-top: 10px;
            }

            ul{
                list-style-type: none;
                margin-top: 10px;

                a{
                    color: $gray;
                    text-decoration: none;
                    font-size: 13px;

                    &:hover{
                        color: $white;
                    }
                }
            }
        }

// terza parte footer

        .social{
            background-color: rgb(52, 52, 52);
            height: 100px;

            .container{
                height: 100%;
            }

            .row{
                @include space_between;
                height: 100%;
            }

            button{
                
                font-size: 20px;
                border: 2px solid $blu;
                padding: 20px;
                background-color: rgb(52, 52, 52);
                @include upbold;

                a{
                    color: $white;
                    text-decoration: none;
                }

                &:hover{
                        font-size: 22px;
                        transition: 0.3s;
                }
            }

            ul{
                display: flex;
                align-items: center;

                h3{
                    @include upbold;
                    color: $blu;
                    padding: 10px;
                }

                li{
                    list-style-type: none;
                    padding: 10px;
                }
            }
        }
</style>

