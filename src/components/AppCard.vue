<script>
export default {
    props: {
        card: Object,
    }
}
</script>

<template>
    <div class="album-card">
        <div class="card">
            <img :src="card.thumb" :alt="card.series">
        </div>
        <h3>{{ card.series }}</h3>  
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

    .album-card{
        width: calc(100% / 6); 
        padding: 10px 10px;

        h3{
            color: $white;
            font-size: 13px;
            @include upbold;
        }
        .card{
            img{
                width: 100%;
            }
            
        }
    }
</style>