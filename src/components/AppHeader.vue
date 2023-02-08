<script>

export default {
    name: 'AppHeader',

}


</script>

<template>
    <header>
        <div class="container">
            <div class="d-flex align-items-center">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/11/Yu-Gi-Oh%21_%28Logo%29.jpg/1200px-Yu-Gi-Oh%21_%28Logo%29.jpg"
                    alt="">
                <h2>
                    Yu-Gi-Oh Api
                </h2>
            </div>
        </div>
    </header>


</template>

<style lang="scss" scoped>
img {
    width: 60px;
    height: 20px;
}

header {
    background-color: $secondary-color;

    .container {
        margin: 0;
    }
}
</style>