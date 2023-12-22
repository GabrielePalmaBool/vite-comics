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
        <img :src="infoComic.thumb" alt="">
        <h3></h3>
    </div>
</template>

<style scoped>
.CmxCard {
    width: 180px;

    padding: 10px;
}
</style>
