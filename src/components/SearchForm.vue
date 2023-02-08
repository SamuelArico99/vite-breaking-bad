<script>

import { store } from "../store";

export default {
    name: 'SearchForm',
    data() {
        return {
            store
        }
    }
}

</script>

<template>

    <h1 class="mt-2">Select an Archetype</h1>
    <form action="">
        <div class="my-container">
            <select v-model="store.statusValue" @change="$emit('search')" class="form-select form-select-sm"
                aria-label="Select status">
                <option selected value="">Select Archetype</option>
                <option value="alien">Alien</option>
                <option value="Ancient%20Gear">Ancient Gear</option>
                <option value="ABC">ABC</option>
            </select>
        </div>
    </form>
</template>

<style lang="scss" scoped>
.my-container {
    padding: 0;
    margin-left: 0;
    padding-left: 60px;
    margin: 40px 0px;
    background-color: $primary-color;
}

select {
    max-width: 20%;
    min-width: 200px;
}

h1 {
    color: $secondary-color;
}
</style>