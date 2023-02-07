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
        <img :src="character.card_images.image_url" class="img-fluid" alt="">
        <div>
            <strong>{{ character.name }}</strong><br>
            <span>{{ character.archetype }}</span>
        </div>
    </div>
</template>

<style lang="scss" scoped>
img {
    width: 100%;
    height: 150px;
}
</style>