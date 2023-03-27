<script>
import { store } from '../store.js';

export default {
    name: 'Card',
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <div class="card">
        <div>img</div>
        <h4>card name</h4>
        <!-- <div> {{ store.archetype }} </div> -->
    </div>
</template>