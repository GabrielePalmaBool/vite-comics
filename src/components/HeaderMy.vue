<script >


export default {
    name: "HeaderMy",

    data() {

        return {

            links: [
                {
                    text: "CHARACTERS",
                    href: "#",
                    current: false
                },
                {
                    text: "COMICS",
                    href: "#",
                    current: true
                },
                {
                    text: "MOVIES",
                    href: "#",
                    current: false
                },
                {
                    text: "TV",
                    href: "#",
                    current: false
                },
                {
                    text: "GAMES",
                    href: "#",
                    current: false
                },
                {
                    text: "COLLECTIBLES",
                    href: "#",
                    current: false
                },
                {
                    text: "VIDEOS",
                    href: "#",
                    current: false
                },
                {
                    text: "FANS",
                    href: "#",
                    current: false
                },
                {
                    text: "NEWS",
                    href: "#",
                    current: false
                },
                {
                    text: "SHOP",
                    href: "#",
                    current: false
                }

            ]

        }
    }
}




</script>

<template>
    <header class="container">

        <!-- Logo sito -->
        <div class="logo">
            <img src="/img/dc-logo.png" alt="">
        </div>

        <!-- navigazione principale -->
        <nav>
            <ul>
                <li v-for="link in links">
                    <a :href="link.href" :class="link.current ? 'active' : ''">
                        <h4>{{ link.text }}</h4>
                    </a>

                </li>

            </ul>
        </nav>

    </header>

    <div class="backgroundHead">

        <header class="container">
            <div class="Second_line">
                <h2> -- Content Goes Here -- </h2>
            </div>
        </header>

    </div>
</template>

<style lang="scss" scoped>
//Scss relativo alla sola sezione di header

@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

header {

    @include center();

    .logo {
        margin: 5px;
        flex-grow: 1;
    }

    nav {

        margin-top: 30px;
        flex-grow: 1;

        ul {

            list-style: none;
            @include center(right);

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
        }
    }



    .Second_line {
        @include center(left);
        flex-grow: 1;
        height: 100px;

        h2 {
            padding: 35px;
            color: white;
            text-align: center;
            font-size: 30px;
        }
    }

}
</style>
