<script>

export default {
    name: 'SearchForm'
}

</script>

<template>
    <div class="my-container">
        <select class="form-select form-select-sm" aria-label=".form-select-sm example">
            <option selected>Open this select menu</option>
            <option value="1">One</option>
            <option value="2">Two</option>
            <option value="3">Three</option>
        </select>
    </div>
</template>

<style lang="scss" scoped>
.my-container {
    padding: 0;
    margin-left: 0;
    padding-left: 60px;
    margin-bottom: 40px;
    background-color: $primary-color;
}

select {
    max-width: 20%;
    min-width: 200px;
}
</style>