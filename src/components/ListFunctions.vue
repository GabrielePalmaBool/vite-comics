<script >
export default {

    name: "ListFunctions"
}
</script>

<template>
    <div class="backgroundMain">

        <main class="container">
            <div class="First_line">
                <nav>
                    <ul>
                        <li>
                            <a href="#">
                                <img src="/img/buy-comics-digital-comics.png" class="logo" alt="logoMain1">
                                <h4>DIGITAL COMICS</h4>
                            </a>

                        </li>
                        <li>
                            <a href="#">
                                <h4>DC MERCHANDISE</h4>
                            </a>

                        </li>
                        <li>
                            <a href="#">
                                <h4>SUBSCRIPTION</h4>
                            </a>

                        </li>
                        <li>
                            <a href="#">
                                <h4>COMIC SHOP LOCATOR</h4>
                            </a>

                        </li>
                        <li>
                            <a href="#">
                                <h4>DC POWER VISA</h4>
                            </a>

                        </li>


                    </ul>
                </nav>
            </div>
        </main>

    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;



main {



    .First_line {

        @include center(left);
        flex-grow: 1;
        height: 100px;

        nav {

            flex-grow: 1;

            ul {

                list-style: none;
                @include center();
                margin: 0;

                li a {

                    margin: 25px;
                    text-decoration: none;

                    .logo {
                        max-width: 70px;
                        max-height: 70px;
                        margin: 10px;
                        vertical-align: middle;
                    }

                    h4 {

                        font-weight: 600;
                        color: white;
                        display: inline-block;

                        vertical-a &.active,
                        &:hover {
                            color: $secondary;
                        }
                    }


                }
            }
        }

    }
}
</style>
