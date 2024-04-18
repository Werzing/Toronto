<template>
    <header class="header">

        <div class="vidio">

            <slot name="vidioBg">

            </slot>

        </div>



        <div class="Fon">
            <div class="wrap">

                <nav id="nav" class="nav">
                    <div class="logo-box">
                        <div class="logo">
                            <a href="/">
                                <img src="/img/Overwatch_2_logo-white-or.png">
                            </a>
                        </div>
                    </div>
                    <ul class="nav__list">
                        <li class="list__item" v-for="navigat in navigation" :key="navigat.id">

                            <NuxtLink :to="`${navigat.link}`">{{ navigat.title }}</NuxtLink>
                        </li>
                    </ul>

                    <a href="https://store.steampowered.com/app/2357570/Overwatch_2/"><button
                            class="play">Играть</button></a>

                </nav>


                <div class="middle">
                    <img src="/img/OW2_Primary_Logo-wide.png" alt="" width="50%">
                    <div>
                        <h1>Играй бесплатно</h1>
                    </div>
                </div>

                <div class="bottom">
                    <a class="bottom__link" :href="`${place.link}`" v-for="place in download" :key="place.id"><img
                            class="bottom__img" :src="`${place.img}`" alt=""></a>
                </div>
            </div>
        </div>

    </header>
</template>











<style scoped>


.Fon{
    width: 100%;
    height: 100%;
    background-color: #02023b33;

}

.vidio {
    width: 100vw;
    height: 90vh;
    position: fixed;
    background-color: #02023b3a;
    z-index: -10;


}


.bottom__link {
    width: 15%;
}

.bottom__img {
    width: 100%;
    transition: 200ms;
}

.bottom__img:hover {
    transform: scale(110%);
}


h1 {
    font-size: 25pt;
}


.play {
    padding: 13px 25px;
    background-color: #ff6400;
    border: none;
    border-radius: 2px;
    font-size: 12pt;
    cursor: pointer;
    transition: 200ms;
}

.play:hover {
    transform: scale(110%);
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    color: white;
}

.header {
    width: 100vw;
    height: 90vh;
    background-attachment: fixed;
    background-size: cover;
    background-position: center;
    background-color: rgba(2, 2, 59, 0.26);
    z-index: 9999;

}

.wrap {
    height: 100%;
    width: 1200px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;

}


.middle {
    height: 20%;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
}

.bottom {
    height: 16%;
    width: 100%;
    display: flex;
    justify-content: space-around;
    align-items: center;
}

.nav {
    width: 100%;
    justify-content: space-evenly;
    align-items: center;
}

.logo-box {
    float: left;
    margin-left: 25px;
    padding: 8px 0;

}

.logo {
    margin: 0;
    height: 70px;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100%;
    width: 100%;
}

.nav,
.nav__list {
    display: flex;
    list-style: none;
    margin: 0;
    padding: 0;

}

.nav__list {
    width: 60%;
    justify-content: space-around;
}

.list__item {
    margin-right: 20px;
    font-size: 14pt;
    transition: 200ms;
}

.list__item:hover {
    transform: scale(110%);
}

nav a {
    text-decoration: none;
}

.middle {
    width: 100%;
    align-self: flex-end;
    text-align: center;
}

.navbar_scrolled {
    width: 100vw;
    /* padding: 20px 0; */
    position: fixed;
    background-color: rgba(60, 71, 68, 0.976);
    animation-name: fadeInUp;
    animation-direction: 1s;
    animation-fill-mode: none;
    transition: 0.3s;
    z-index: 9999;
}


@keyframes fadeInUp {
    0% {
        opacity: 0;
        top: -50px;


    }

    100% {
        opacity: 1;
        top: 0px;
    }

}
</style>












<script>




export default {
    data() {
        return {
            navigation: [
                {
                    id: 0,
                    title: "Главная",
                    link: "/",
                    nuxt: true,
                },
                {
                    id: 1,
                    title: "Герои",
                    link: "/heroes",
                    nuxt: true,
                },
                {
                    id: 2,
                    title: "Режимы",
                    link: "/#modes",
                    nuxt: false,
                },
                {
                    id: 3,
                    title: "Классы",
                    link: "/#role",
                    nuxt: false,
                },
                {
                    id: 4,
                    title: "Киберспорт",
                    link: "/sport",
                    nuxt: true,
                },

            ],



            download: [
                {
                    id: 0,
                    img: "/img/nintendo.png",
                    link: "https://www.nintendo.com/us/store/products/overwatch-2-switch/",
                },
                {
                    id: 1,
                    img: "/img/pngegg.png",
                    link: "https://eu.account.battle.net/login/ru/challenge/1e8ed7ec-cc21-435d-8d0b-64437bedc35f?ref=https://eu.shop.battle.net/ru-ru/product/overwatch?blzcmp%3Dow_gamesite%26_gl%3D1*192eefj*_ga*MTkxODIyNjM2NC4xNzA3OTMxMjMw*_ga_VYKNV7C0S3*MTcwODc4ODIxMC4xMS4xLjE3MDg3ODgyMjMuNDcuMC4w&externalChallenge=legal&app=mktp",
                },
                {
                    id: 2,
                    img: "/img/PS5-XSX-XSS.png",
                    link: "https://www.xbox.com/ru-RU/games/store/overwatch-origins-edition/C1C4DZJPBC2V/0001",
                },
                {
                    id: 3,
                    img: "/img/PlayStation-Logo-PNG.png",
                    link: "https://store.playstation.com/en-gb/error",
                },
                {
                    id: 4,
                    img: "/img/Steam-Logo-PNG.png",
                    link: "https://store.steampowered.com/app/2357570/Overwatch_2/",
                },
            ]
        }
    },

    methods: {
        handleScroll() {
            let navbar = document.getElementById("nav").classList
            let actve_class = "navbar_scrolled"

            if (scrollY > 400) navbar.add(actve_class)
            else navbar.remove(actve_class)
        },


    },
    created() {
        if (process.client) {
            window.addEventListener('scroll', this.handleScroll);
        }
    },
    destroyed() {
        if (process.client) {
            window.removeEventListener('scroll', this.handleScroll);
        }
    },
    mounted() {
        document.title = "Overwatch 2"
    },



}
</script>



