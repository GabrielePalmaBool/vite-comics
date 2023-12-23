<script >
export default {

    name: "ListFunctions",

    data() {

        return {

            links: [
                {
                    title: "DIGITAL COMICS",
                    href: "/img/buy-comics-digital-comics.png",
                },
                {
                    title: "DC MERCHANDISE",
                    href: "/img/buy-comics-merchandise.png",
                },
                {
                    title: "SUBSCRIPTION",
                    href: "/img/buy-comics-subscriptions.png",
                },
                {
                    title: "COMIC SHOP LOCATORS",
                    href: "/img/buy-comics-shop-locator.png",
                },
                {
                    title: "DC POWER VISA",
                    href: "/img/buy-comics-digital-comics.png",
                }
            ]
        }
    }
}



</script>

<template>
    <div class="backgroundMain">

        <main class="container">
            <div class="First_line">
                <nav>
                    <ul>
                        <li v-for="link in links">
                            <a :href="link.href">
                                <img :src="link.href" class="logo" alt="logoMain1">
                                <h4>{{ link.title }}</h4>
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

.backgroundMain {
    background-color: $secondary;
}

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
                margin-top: 20px;

                li a {

                    margin: 10px;
                    text-decoration: none;

                    .logo {
                        max-width: 70px;
                        max-height: 70px;
                        padding: 5px;
                        vertical-align: middle;
                    }

                    h4 {

                        font-weight: 600;
                        color: $tertiary;
                        display: inline-block;

                        &.active,
                        &:hover {
                            color: $primary;
                        }

                    }

                }
            }
        }

    }
}
</style>
