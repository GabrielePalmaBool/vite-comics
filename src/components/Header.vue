<script >


export default {
    name: "Header"
}


</script>

<template>
    <header>

    </header>
</template>

<style lang="scss" scoped>
//Scss relativo alla sola sezione di header

@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

header {



    ul {

        text-align: right;

        list-style: none;
        margin: 2.5rem 1rem 4rem;
        @include center(right);

        li a {

            display: inline-block;
            padding: 1rem;
            text-decoration: none;
            font-weight: 600;
            transition: background 0.3s;

            &.active,
            &:hover {
                background: $secondary;
            }
        }
    }

}
</style>
