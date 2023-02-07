<script>

import CharacterCard from './CharacterCard.vue'
import SearchForm from './SearchForm.vue';

export default {
    name: 'AppMain',
    props: {
        charactersList: {
            type: Array,
            default: []
        },
        charactersCount: {
            type: Number,
            default: 0
        }
    },
    components: {
        SearchForm,
        CharacterCard
    }
}

</script>

<template>
    <main>
        <SearchForm />
        <div class="container">
            <div class="my-row d-flex align-items-center">
                <h3>
                    Found {{ charactersCount }} cards
                </h3>
            </div>
            <div class="row row-cols-2 row-cols-sm-3 row-cols-md-4 row-cols-lg-5">
                <div class="col" v-for="character in charactersList">
                    <CharacterCard :character="character" />
                </div>
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
main {
    width: 100%;
    background-color: $primary-color;
    padding: 10px;

    .container {
        background-color: white;
        padding: 20px;

        .my-row {
            height: 60px;
            width: 100%;
            background-color: $third-color;
            color: white;
            padding: 10px;
        }
    }
}

.card {
    background-color: $primary-color;
    border-radius: 0px;
    margin-bottom: 10px;
}
</style>