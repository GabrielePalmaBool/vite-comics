<script >
export default {

    name: "FooterMy",

    // components: {
    //     ComixCard
    // },

    data() {

        return {

            linksCol1: [
                {
                    text: "Characters",
                    href: "#",
                    current: false
                },
                {
                    text: "Comics",
                    href: "#",
                    current: true
                },
                {
                    text: "Movies",
                    href: "#",
                    current: false
                },
                {
                    text: "Tv",
                    href: "#",
                    current: false
                },
                {
                    text: "Games",
                    href: "#",
                    current: false
                },
                {
                    text: "Video",
                    href: "#",
                    current: false
                },
                {
                    text: "News",
                    href: "#",
                    current: false
                }

            ],

            linksCol2: [
                {
                    text: "Terms of Use",
                    href: "#",
                    current: false
                },
                {
                    text: "Privacy Policy (New)",
                    href: "#",
                    current: true
                },
                {
                    text: "Ad Choices",
                    href: "#",
                    current: false
                },
                {
                    text: "Advertising",
                    href: "#",
                    current: false
                },
                {
                    text: "Jobs",
                    href: "#",
                    current: false
                },
                {
                    text: "Subscriptions",
                    href: "#",
                    current: false
                },
                {
                    text: "Talent Workshops",
                    href: "#",
                    current: false
                }, {
                    text: "CPSC Certificates",
                    href: "#",
                    current: false
                },
                {
                    text: "Ratings",
                    href: "#",
                    current: false
                },
                {
                    text: "Shop Help",
                    href: "#",
                    current: false
                },
                {
                    text: "Contact Us",
                    href: "#",
                    current: false
                }

            ],

            linksCol3: [
                {
                    text: "DC",
                    href: "#",
                    current: false
                },
                {
                    text: "Mad Magazine",
                    href: "#",
                    current: true
                }, {
                    text: "DC Kids",
                    href: "#",
                    current: false
                },
                {
                    text: "DC Universe",
                    href: "#",
                    current: false
                }, {
                    text: "DC Power Visa",
                    href: "#",
                    current: false
                }

            ],

            linksCol4: [
                {
                    text: "Shop DC",
                    href: "#",
                    current: false
                },
                {
                    text: "Shop DC Collectibles",
                    href: "#",
                    current: true
                }

            ]
        }
    }

}

</script>

<template>
    <div class="backgroundFoot1">

        <footer class="container">

            <!-- navigazione principale Colonna 1 -->
            <nav>
                <div class="col">
                    <h2>DC COMICS</h2>
                    <ul>
                        <li v-for="link in linksCol1">
                            <a :href="link.href" :class="link.current ? 'active' : ''">
                                <p>{{ link.text }}</p>
                            </a>

                        </li>
                    </ul>

                </div>

                <div class="col">
                    <h2>DC</h2>
                    <ul>
                        <li v-for="link in linksCol2">
                            <a :href="link.href" :class="link.current ? 'active' : ''">
                                <p>{{ link.text }}</p>
                            </a>

                        </li>
                    </ul>

                </div>

                <div class="col">
                    <h2>SITE</h2>
                    <ul>
                        <li v-for="link in linksCol3">
                            <a :href="link.href" :class="link.current ? 'active' : ''">
                                <p>{{ link.text }}</p>
                            </a>

                        </li>
                    </ul>

                </div>

                <div class="subcol">
                    <h2>SITE</h2>
                    <ul>
                        <li v-for="link in linksCol4">
                            <a :href="link.href" :class="link.current ? 'active' : ''">
                                <p>{{ link.text }}</p>
                            </a>

                        </li>
                    </ul>

                </div>

            </nav>

            <!-- Logo footer DC -->
            <div class="Logo"></div>

        </footer>

    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

.backgroundFoot1 {
    background-image: url("/img/footer-bg.jpg");
    min-height: 500px;
    background-repeat: no-repeat;
    background-size: 100% 100%;
}


footer {

    @include center();

    position: relative;

    nav {
        display: flex;
        flex-wrap: wrap;
        flex-basis: 100%;

        .col {
            flex-basis: 17%;
            margin-top: 70px;
        }

        .subcol {
            flex-basis: 100%;
            margin-top: -95px;
        }

        h2 {
            color: $tertiary;

        }

        ul {

            list-style: none;

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
        }
    }


    .Logo {
        position: absolute;
        top: 0;
        right: 0;
        background-image: url("/img/dc-logo-bg.png");
        width: 560px;
        height: 500px;
    }
}
</style>
