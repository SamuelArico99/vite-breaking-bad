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
.card {
    min-height: 250px;
}

.text-information {
    padding: 5px;
    text-align: center;
    font-size: 12px;

    strong {
        color: $secondary-color;
    }
}
</style>