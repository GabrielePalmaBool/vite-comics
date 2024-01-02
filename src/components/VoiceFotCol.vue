<script >

export default {
    name: "VoiceFotCol",

    props: {
        linkVoice: Object
    }
}

</script>

<template>
    <li>
        <a :href="linkVoice.href" :class="linkVoice.current ? 'active' : ''">
            <p>{{ linkVoice.text }}</p>
        </a>

    </li>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;


li a {

    display: inline-block;
    padding: 5px;
    text-decoration: none;
    color: $tertiary;

    &.active {
        color: $secondary;
    }

    p {

        font-weight: 600;

        &.active,
        &:hover {
            color: $secondary;
        }
    }

}
</style>
