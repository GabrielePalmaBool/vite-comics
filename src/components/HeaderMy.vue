<script >


export default {
    name: "HeaderMy"
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
