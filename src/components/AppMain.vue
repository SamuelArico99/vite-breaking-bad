<script>

import SearchForm from './SearchForm.vue';

export default {
    name: 'AppMain',
    components: {
        SearchForm
    }
}

</script>

<template>
    <main>
        <SearchForm />
        <div class="container">
            <div class="my-row d-flex align-items-center">
                <h3>
                    Found 39 cards
                </h3>
            </div>
            <div class="row row-cols-2 row-cols-sm-3 row-cols-md-4 row-cols-lg-5">
                <div class="col" v-for="i in 40">
                    <div class="card">
                        <img src="https://via.placeholder.com/150" class="img-fluid" alt="">
                        <div>
                            <strong>Character Name</strong><br>
                            <span>Character Species</span>
                        </div>
                    </div>

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
    margin: 10px 0px;
}
</style>