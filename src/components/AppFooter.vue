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
    methods: {
        getImagePath: function (img) {
            return `/img/${img}`
        }
    }
    
}
</script>

<template lang="">
    <footer>
        <div class="bg-blu">
            <div class="container">
               <div class="row">
                    <div class="col">
                        <ul>
                            <li v-for="(i, index) in icon" :key="i">
                                <a href="#">
                                    
                                    <img :src="getImagePath(i.label)" alt="logo">
                                    
                                    <span>{{i.description}}</span>
                                </a>
                            </li>
                        </ul>
                    </div>
               </div>
            </div>
        </div>
        <div class="jumbo">
            <div class="container">
               
            </div>

        </div>
        <div class="social">
            <div class="container">
               
            </div>

        </div>
    </footer>
</template>

<style lang="scss">
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;
    
        .bg-blu{
            background-color: $blu;
           
            .row{
                
                ul{
                    @include space_between;
                }
                li{
                    @include space_between;
                    padding: 30px;
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
                }
            }

        }

</style>

