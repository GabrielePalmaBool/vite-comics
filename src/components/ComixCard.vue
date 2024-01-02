<script >

export default {
    name: "ComixCard",

    props: {
        infoComic: Object
    }
}

</script>

<template>
    <li v-if="infoComic.href">
        <a :href="infoComic.href" :class="infoComic.current ? 'active' : ''">
            <h4>{{ infoComic.text }}</h4>
        </a>

    </li>
    <div class="CmxCard" v-else>
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

    a {
        text-decoration: none;

        h3 {
            color: $tertiary;
            text-align: center;
            font-size: 17px;
            cursor: pointer;
            font-weight: bold;
        }

        h3:hover {
            color: $secondary;
        }
    }

}

li a {

    display: inline-block;
    padding: 10px;
    text-decoration: none;

    &.active {
        color: $secondary;
    }

    h4 {

        font-weight: 600;

        &.active,
        &:hover {
            color: $secondary;
        }
    }


}
</style>
