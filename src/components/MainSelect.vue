<script>
    import { store } from '../store';

    export default {
        name: 'Main Select',
        data() {
            return {
                store
            }
        }
    }
</script>

<template>
    <div>
        <label for="select"></label>
        <select id="select" @change="$emit('search')" v-model="store.searchStatus">
            <option selected value="">All Cards</option>
            <option value="Alien">Alien</option>
            <option value="Noble Knight">Noble Knight</option>
            <option value="Melodious">Melodious</option>
            <option value="Archfiend">Archfiend</option>
            <option value="Elemental HERO">Elemental HERO</option>
            <option value="Umi">Umi</option>
            <option value="ABC">ABC</option>
        </select>
    </div>
</template>

<style lang="scss" scoped>
    div {
        margin-left: 1.0625rem;
        margin-bottom: 1.875rem;

        select {
            width: 15rem;
            padding: .75rem .3125rem;
            font-size: 1.2em;
            border-radius: .625rem;
            cursor: pointer;
            border: none;
        }
    }
</style>