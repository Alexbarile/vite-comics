<script>
export default {
    
}
</script>

<template lang="">
    <main>
        <div class="container">
            <div class="row">
                <div class="col">
                    <span>Content goes here</span>
                </div>
            </div>
        </div>
    </main>
</template>

<style lang="scss">
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;
    
    main{
        background-color: $black;
        height: 100px;
        @include space_between;
        
        span{
            color: white;
        }
    }
</style>