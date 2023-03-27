<script>
    import Card from './Card.vue';

    export default {
        name: 'Main Cards List',
        component: {
            Card
        }
    }
</script>

<template>
    <div class="container-mid">
        <h3 class="cards-found">
            Found 39 cards
        </h3>
        <div class="cards-list">
            <div class="card">
                <div>img</div>
                <h4>card name</h4>
                <div>type</div>
            </div>
            <div class="card">
                <div>img</div>
                <h4>card name</h4>
                <div>type</div>
            </div>
            <div class="card">
                <div>img</div>
                <h4>card name</h4>
                <div>type</div>
            </div>
            <div class="card">
                <div>img</div>
                <h4>card name</h4>
                <div>type</div>
            </div>
            <div class="card">
                <div>img</div>
                <h4>card name</h4>
                <div>type</div>
            </div>
            <div class="card">
                <div>img</div>
                <h4>card name</h4>
                <div>type</div>
            </div>
            <div class="card">
                <div>img</div>
                <h4>card name</h4>
                <div>type</div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    @use '../assets/scss/_partials/mixins.scss' as *;
    @use '../assets/scss/_partials/variables.scss' as *;

    .container-mid {
        background-color: #fff;
        padding: 4.375rem;
        .cards-found {
            padding: 2.1875rem 1.875rem 1.875rem;
            background-color: #212529;
            color: #fff;
        }

        .cards-list {
            display: flex;
            flex-wrap: wrap;
            margin: 0 -1.0938rem;
            .card {
                background-color: var(--primary-color);
                width: calc(100% / 5 - 35px);
                margin: 0 1.0938rem 1.5625rem;
            }
        }
    }
</style>