<script >


export default {
    name: "Header"
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
                <li>
                    <a href="#">
                        <h4>CHARACTERS</h4>
                    </a>

                </li>
                <li>
                    <a href="#">
                        <h4>COMICS</h4>
                    </a>

                </li>
                <li>
                    <a href="#">
                        <h4>MOVIES</h4>
                    </a>

                </li>
                <li>
                    <a href="#">
                        <h4>TV</h4>
                    </a>

                </li>
                <li>
                    <a href="#">
                        <h4>GAMES</h4>
                    </a>

                </li>
                <li>
                    <a href="#">
                        <h4>COLLECTIBLES</h4>
                    </a>

                </li>
                <li>
                    <a href="#">
                        <h4>VIDEOS</h4>
                    </a>

                </li>
                <li>
                    <a href="#">
                        <h4>FANS</h4>
                    </a>

                </li>
                <li>
                    <a href="#">
                        <h4>NEWS</h4>
                    </a>

                </li>
                <li>
                    <a href="#">
                        <h4>SHOP</h4>
                    </a>

                </li>

            </ul>
        </nav>

    </header>
</template>

<style lang="scss" scoped>
//Scss relativo alla sola sezione di header

@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

header {

    @include center();

    .logo {
        margin-top: 30px;
        @include center(left);
        flex-basis: 50%;
    }


    ul {

        list-style: none;
        margin-top: 60px;
        @include center(right);
        flex-basis: 50%;

        li a {

            display: inline-block;
            padding: 10px;
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
