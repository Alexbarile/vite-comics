<script>
export default {
    
}
</script>

<template>
    <header class="container">
        <div class="row">

            <div class="col">
                <a href="#" class="logo">
                    <img src="../../public/img/dc-logo.png" alt="logo">
                </a>
            </div>

            <div class="col">
                <ul>
                    <li>ciao</li>
                </ul>
            </div>
        </div>
    </header>
</template>

<style lang="scss">
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;

    .row{
        @include space_between;
        margin-top: 20px 
    }
    .col{
        @include space_between;
    }
</style>