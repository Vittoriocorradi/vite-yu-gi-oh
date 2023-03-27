<script>
    export default {
        name: 'Header',
    }
</script>

<template>
    <header>
        <div class="img">
            logo
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
        }
    }
</style>