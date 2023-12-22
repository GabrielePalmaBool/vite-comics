<script >

export default {
    name: "ComixCard",

    props: {
        infoComic: Object
    }
}

</script>

<template>
    <div class="CmxCard">
        <a :href="infoComic.thumb">
            <img :src="infoComic.thumb" alt="immagine fumetto">
            <h3>{{ infoComic.series }}</h3>
        </a>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

.CmxCard {
    width: 180px;
    padding: 10px;
    margin: 30px 0px 10px 0px;

    h3 {
        color: $tertiary;
        text-align: center;
        font-size: 17px;
    }
}
</style>
