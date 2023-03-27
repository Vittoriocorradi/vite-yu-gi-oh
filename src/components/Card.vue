<script>
import { store } from '../store.js';

export default {
    name: 'Card',
    data() {
        return {
            store
        }
    },
    props: {
        img: String,
        name: String,
        archetype: String
    }
}
</script>

<template>
    <div class="card">
        <div class="img">
            <img :src="img" alt="">
        </div>
        <div class="text">
            <h4> {{ name }} </h4>
            <div> {{ archetype }} </div>
        </div>
    </div>
</template>