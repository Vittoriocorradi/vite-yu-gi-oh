<script>
import MainSelect from './MainSelect.vue';
import MainCardsList from './MainCardsList.vue';

export default {
    name: 'Main',
    components: {
        MainSelect,
        MainCardsList
    },
    // methods: {
    //     tada() {
    //         console.log('yadayada');
    //         this.$emit('search');
    //     }
    // }
}
</script>

<template>
    <main>
        <div class="container">
            <MainSelect @search="$emit('search')"/>
            <MainCardsList />
        </div>
    </main>
</template>

<style lang="scss">
@use '../assets/scss/_partials/mixins.scss' as *;
@use '../assets/scss/_partials/variables.scss' as *;


main {
    background-color: var(--primary-color);
    padding: 2.1875rem 10rem 0;

    .container {
        @include my-container(105rem);
    }
}


</style>