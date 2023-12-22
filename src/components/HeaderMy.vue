<script >
import ComixCard from './ComixCard.vue'

export default {
    name: "HeaderMy",
    components: {
        ComixCard
    },

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

            ],

            comixs: [
                {
                    thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    price: "$19.99",
                    series: "Action Comics",
                    type: "comic book",
                },
                {
                    thumb: "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    price: "$3.99",
                    series: "American Vampire 1976",
                    type: "comic book",
                },
                {
                    thumb: "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    price: "$16.99",
                    series: "Aquaman",
                    type: "graphic novel",
                },
                {
                    thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    price: "$2.99",
                    series: "Batgirl",
                    type: "comic book",
                },
                {
                    thumb: "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    price: "$3.99",
                    series: "Batman",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    price: "$2.99",
                    series: "Batman Beyond",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    price: "$3.99",
                    series: "Batman/Superman",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    price: "$4.99",
                    series: "Batman/Superman Annual",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    price: "$5.99",
                    series: "Batman: The Joker War Zone",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    price: "$6.99",
                    series: "Batman: Three Jokers",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    price: "$4.99",
                    series: "Batman: White Knight Presents: Harley Quinn",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    price: "$16.99",
                    series: "Catwoman",
                    type: "graphic novel",
                },
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

    <!-- Seconda Sezione header  Black-->
    <div class="backgroundHead">


        <header class="container">

            <div class="Current_list">
                <h2>CURRENT SERIES</h2>
            </div>

            <div class="Second_line">

                <!-- Richiamo il mio componente che dovrà ripetersi -->
                <ComixCard v-for="(Com, i) in comixs" :key="i" :infoComic="Com" />

            </div>

            <div class="Load">
                <a href="#">Load more</a>
            </div>

        </header>

    </div>
</template>

<style lang="scss" scoped>
//Scss relativo alla sola sezione di header

@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

.backgroundHead {
    background-color: $primary;
}

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

    .Current_list {
        margin: -20px 550px 0px 0px;
        padding: 10px;
        width: 230px;
        font-weight: bold;
        background-color: $secondary;

        h2 {
            color: $tertiary;
        }
    }

    .Second_line {
        @include center();
        margin: 10px 0px 40px 0px;
    }

    .Load {

        margin: 10px 0px 30px 0px;


        a {
            text-decoration: none;
            color: $tertiary;
            cursor: pointer;
            font-size: 20px;
            font-weight: bold;
            padding: 5px 15px 5px 15px;
            background-color: $secondary;

        }

        a:hover {
            color: $primary;
        }
    }

}
</style>
