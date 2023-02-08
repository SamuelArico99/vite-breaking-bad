<script>

export default {
    name: 'CharacterCard',
    props: {
        character: Object
    }
}

</script>

<template>
    <div class="card">
        <img :src="character.card_images[0].image_url" class="img-fluid" alt="">
        <div class="text-information">
            <strong>{{ character.name }}</strong><br>
            <span>{{ character.archetype }}</span>
        </div>
    </div>
</template>

<style lang="scss" scoped>
img {
    width: 100%;
    height: 225px;
}

.card {
    min-height: 300px;
    max-height: 300px;
}

.text-information {
    padding: 5px;
    text-align: center;

    strong {
        color: $secondary-color;
    }
}
</style>