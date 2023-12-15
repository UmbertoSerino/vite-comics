<script>
export default {
    name: 'HeoresCard',
    data() {
        return {

        }
    },
    props: [
        'imageHero',
        'title',
        'price',
        'type'
    ]

}


</script>

<template>
    <article>
        <img class="card-pictures" :src="imageHero" alt="">
        <p>{{ title }}</p>

    </article>
</template>



<style lang="scss">
article {
    width: 150px;
    height: 150px;
}

img.card-pictures {
    width: 100%;
    height: 100%;

}
</style>