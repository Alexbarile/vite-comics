<script>
export default {
    data() {
        return {
            menu: [
                {
                    label: 'Characters',
                    url: '#',
                    active: false
                },
                {
                    label: 'Comics',
                    url: '#',
                    active: true
                },
                {
                    label: 'Movies',
                    url: '#',
                    active: false
                },
                {
                    label: 'Tv',
                    url: '#',
                    active: false
                },
                {
                    label: 'Games',
                    url: '#',
                    active: false
                },
                {
                    label: 'Collectibles',
                    url: '#',
                    active: false
                },
                {
                    label: 'Videos',
                    url: '#',
                    active: false
                },
                {
                    label: 'Fans',
                    url: '#',
                    active: false
                },
                {
                    label: 'News',
                    url: '#',
                    active: false
                },
                {
                    label: 'Shop',
                    url: '#',
                    active: false
                }
            ]
        }
    },
    
}
</script>

<template>
    <header class="container">
        <div class="row-header">

            <div class="col-header">
                <a href="#" class="logo">
                    <img src="../../public/img/dc-logo.png" alt="logo">
                </a>
            </div>

            <div class="col-header">
                <ul>
                    <li v-for="(item, index) in menu" :key="index">
                        <a href="item.url" class="item.active ? 'active' : ''">
                            {{ item.label }}
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </header>
</template>

<style lang="scss">
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

    .row-header{
        @include space_between;
        margin-top: 20px 
    }
    .col-header{
        @include space_between;
    }
    ul{
        @include center;
        list-style-type: none;
        li{
            padding: 10px;
            @include upbold;
            a{
                text-decoration: none;
                color: black;

                &.active, &:hover{
                    color: $primary;
                    border-bottom: 5px solid $primary;
                    padding-bottom: 40px;
                }
            }
        }
    }
</style>