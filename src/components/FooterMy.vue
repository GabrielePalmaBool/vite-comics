<script >

import VoiceFotCol from './VoiceFotCol.vue'

export default {

    name: "FooterMy",

    components: {
        VoiceFotCol
    },

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
                        <!-- Richiamo il mio componente che dovrà ripetersi per col1-->
                        <VoiceFotCol v-for="(link, i) in linksCol1" :key="i" :linkVoice="link" />
                    </ul>

                </div>

                <div class="col">
                    <h2>DC</h2>
                    <ul>
                        <!-- Richiamo il mio componente che dovrà ripetersi per col2-->
                        <VoiceFotCol v-for="(link, i) in linksCol2" :key="i" :linkVoice="link" />
                    </ul>

                </div>

                <div class="col">
                    <h2>SITE</h2>
                    <ul>
                        <!-- Richiamo il mio componente che dovrà ripetersi per col3-->
                        <VoiceFotCol v-for="(link, i) in linksCol3" :key="i" :linkVoice="link" />
                    </ul>

                </div>

                <div class="subcol">
                    <h2>SITE</h2>
                    <ul>
                        <!-- Richiamo il mio componente che dovrà ripetersi per col4-->
                        <VoiceFotCol v-for="(link, i) in linksCol4" :key="i" :linkVoice="link" />
                    </ul>

                </div>

            </nav>

            <!-- Logo footer DC -->
            <div class="Logo"></div>

        </footer>
    </div>

    <!-- Secondo footer  -->
    <div class="backgroundFoot2">
        <!-- Secondo footer  -->
        <footer class="container">

            <div class="SignUp">
                <a href="#">
                    <p>SIG UP NOW!</p>
                </a>
            </div>

            <div class="FollowUs">

                <h2>FOLLOW US</h2>

                <div class="icon">
                    <a href="#">
                        <img src="/img/footer-facebook.png" alt="LogoFooter1">
                    </a>
                    <a href="#">
                        <img src="/img/footer-periscope.png" alt="LogoFooter2">
                    </a>
                    <a href="#">
                        <img src="/img/footer-pinterest.png" alt="LogoFooter3">
                    </a>
                    <a href="#">
                        <img src="/img/footer-twitter.png" alt="LogoFooter4">
                    </a>
                    <a href="#">
                        <img src="/img/footer-youtube.png" alt="LogoFooter5">
                    </a>
                </div>

            </div>

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

.backgroundFoot2 {
    background-color: rgb(48, 48, 48);
    min-height: 100px;
    background-repeat: no-repeat;
    background-size: 100% 100%;
}

footer {

    position: relative;

    @include center();

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

    .SignUp {

        flex-basis: 50%;
        margin-top: 30px;

        a {

            padding: 15px 20px 15px 20px;
            text-decoration: none;
            border: 2px solid $secondary;
            color: $tertiary;
            cursor: pointer;
            font-size: 20px;
            font-weight: bold;

            p {
                display: inline-block;
            }
        }

        a:hover {
            color: $secondary;
        }

    }

    .FollowUs {
        margin-top: 30px;
        flex-basis: 50%;

        h2 {
            display: inline;
            color: $secondary;

        }

        .icon {

            margin: -30px 0px 0px 155px;
            vertical-align: middle;

            a {
                cursor: pointer;
                margin: 10px;

            }
        }

    }
}
</style>
