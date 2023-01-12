<script>
export default {
    props: {
        name: 'AppCard',
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
    
</style>