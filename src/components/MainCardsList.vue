<script>
import Card from './Card.vue';
import { store } from '../store.js';


export default {
    name: 'Main Cards List',
    components: {
        Card
    },
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <div class="container-mid">
        <h3 class="cards-found">
            Found {{ store.cardsCut.length }} cards
        </h3>
        <div class="well" v-if="store.cardsCut.length !== 40">
                    <i class="ex-10-icon fas fa-circle-notch"></i>
        </div>
        <div class="cards-list" v-else>
            <Card v-for="card in store.cardsCut" :img="card.card_images[0].image_url" :name="card.name"
                :archetype="card.archetype" />
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

        :deep(.card) {
            background-color: var(--primary-color);
            width: calc(100% / 5 - 35px);
            margin: 0 1.0938rem 1.5625rem;
            text-align: center;

            .img {

                img {
                    max-width: 100%;
                }
            }

            .text {
                padding: 1.875rem 1.875rem 2.8125rem;

                h4 {
                    color: #fff;
                    margin-bottom: 2.1875rem;
                    text-transform: uppercase;
                }
            }
        }
    }
}

.ex-10-icon {
    font-size: 60px;
    animation-name: circle-counter-clockwise;
    animation-duration: 1s;
    animation-iteration-count: infinite;
    animation-timing-function: linear;
    display: flex;
    justify-content: center;
    margin-top: 3.125rem;
    color: var(--primary-color);
}

@keyframes circle-counter-clockwise {
    0% {
        transform: rotate(0deg);
    }

    100% {
        transform: rotate(360deg);
    }
}
</style>