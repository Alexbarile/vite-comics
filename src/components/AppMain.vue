<script>
import AppCard from './AppCard.vue';

export default {
    components: {
        AppCard,
    },
    data() {
        return {
            Cards: [
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
                }
            ]
        };
    },
}
</script>

<template>
    <main>
        
        <!-- jumbotron -->

        <div class="jumbo">
        </div>

        <!-- serie tv -->

        <div class="bg-black">
            <div class="container">
                <div class="row">
                    <div class="col-info">
                        <h4>Current series</h4>
                    </div>
                </div>
                <div class="row">
                    <div class="col">
                        <AppCard v-for="(item, index) in Cards" :key="index" :card="item"></AppCard> 
                    </div>
                </div>
                <div class="row">
                    <div class="col">
                        <button><a href="#">Load More</a></button>
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;
    
    main{
        .jumbo{
            height: 350px;
            width: 100%;
            background-image: url('../../public/img/jumbotron.jpg');
            background-size: cover;
        }
        .bg-black{
            background-color: rgb(31, 31, 31);

            .container{
                .row{
                    width: 100%;

                    .col-info{
                        display: flex;
                        justify-content: flex-start;
                        position: relative;

                        h4{
                            font-size: 25px;
                            padding: 7px 40px;
                            background-color: $blu;
                            position: absolute;
                            top: -27px;
                            @include upbold;
                            color: $white;  
                        }
                    }
                    .col{
                        width: 100%;
                        display: flex;
                        align-items: baseline;
                        flex-wrap: wrap;
                        padding-top: 30px
                    }
                }
            }
            .col{
                @include center;

                button{
                    padding: 7px 40px;
                    background-color: $blu;
                    border: none;
                    margin-bottom: 20px;
                    
                    &:hover{
                        box-shadow: 0 0 7px 5px rgba(255, 255, 255, 0.423);
                    }
    
                    a{
                        text-decoration: none;
                        @include upbold;
                        color: $white;
                        font-size: 13px;
                    }
                }
            } 
        }
    }
</style>