<script>
import axios from 'axios';
import { store } from "../store";
import CharacterCard from './CharacterCard.vue'
import SearchForm from './SearchForm.vue';


export default {
    name: 'AppMain',
    data() {
        return {
            store
        }
    },
    methods: {
        getArchetype() {
            console.log('ciao');
            axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?archetype=' + this.store.statusValue)
                .then((response) => {
                    console.log(response.data.data.slice(0, 40));
                    this.store.results = response.data.data.slice(0, 40)
                });

        }
    },
    created() {
        this.getArchetype();
    },
    components: {
        SearchForm,
        CharacterCard
    }
}

</script>

<template>
    <main>
        <SearchForm @search="getArchetype" />
        <div class="container">
            <div class="my-row d-flex align-items-center">
                <h3>
                    Found {{ store.results.length }} cards
                </h3>
            </div>
            <div class="row row-cols-2 row-cols-sm-3 row-cols-md-4 row-cols-lg-5">
                <div class="col" v-for="character in store.results">
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