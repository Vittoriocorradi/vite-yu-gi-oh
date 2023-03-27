<script>
    export default {
        name: 'Header',
    }
</script>

<template>
    <header>
        <div class="img">
            <img src="http://vignette1.wikia.nocookie.net/yugiohenespanol/images/a/aa/Yugioh_anime_logo.jpg/revision/latest?cb=20130310042737&path-prefix=es" alt="">
        </div>
        <h1>
            Yu-Gi-Oh Api
        </h1>
    </header>
</template>

<style lang="scss" scoped>
    header {
        padding: 1.875rem 2.5rem;
        display: flex;
        align-items: center;

        .img {
            margin-right: 1.0625rem;
            width: 4.6875rem;

            img {
                max-width: 100%;
            }
        }
    }
</style>