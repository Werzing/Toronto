<template>
    <footer class="footer">
        <div class="wrap">
            <div class="wrap__content">
                <div class="wrap-left">
                    <div class="wrap-left__logo"><a href="https://www.blizzard.com/ru-ru/"
                            class="wrap-left__logo__link"><img class="wrap-left__logo__link__img"
                                src="/img/footr__logo.png" alt=""></a></div>
                    <div class="wrap-left__text">
                        <span>© Blizzard Entertainment, Inc., 2024</span>
                        <p>Все упомянутые товарные знаки являются собственностью соответствующих владельцев.</p>
                        <p>Этот веб-сайт был разработан как дипломный проект и не преследует коммерческих целей.</p>
                    </div>
                </div>

                <div class="wrap-right">
                    <ul class="footer__list">
                        <li class="list__item" v-for="href in hrefs" :key="hrefs.id">
                            <a :href="`${href.link}`" class="list__item-link"><img :src="`${href.img}`" alt=""
                                    class="list__item-img"></a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>


    </footer>
</template>



<style scoped>
* {
    color: #8a8d98;
}

@media screen and (min-width: 1200px) {
    ul,
    li,
    a {
        text-decoration: none;
        list-style: none;
    }

    .footer {
        width: 100vw;
        height: 20vh;
        background: linear-gradient(90deg, rgba(18, 21, 36, 1) 0%, rgba(36, 42, 66, 1) 50%, rgba(18, 21, 36, 1) 100%);
    }

    .wrap {
        width: 1200px;
        margin: 0 auto;
        height: 100%;
    }

    .wrap__content {
        width: 100%;
        height: 90%;
        display: flex;
        align-items: center;
        justify-content: space-between;

    }

    .wrap-left {
        height: 100%;
        width: 66%;
        display: flex;
        align-items: center;
    }

    .wrap-left__logo {
        height: 100%;
        width: 20%;
        display: flex;
        align-items: center;
    }

    .wrap-left__text {
        font-size: 12px;
        color: #8a8d98;
        line-height: 25px;
    }

    .wrap-right {
        width: 15%;
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: space-evenly;
    }


    .footer__list {
        display: flex;
        align-items: center;
        justify-content: space-evenly;
    }

    .list__item {
        width: 100%;
    }

    .list__item-link {
        width: 100%;
    }

    .list__item-img {
        width: 70%;
    }

    .wrap-left__logo__link {
        width: 50%;
        height: 50%;
        display: flex;
        align-items: center;
    }

    .wrap-left__logo__link__img {
        width: 200%;
    }

}

@media screen and (max-width:1199px) and (min-width: 901px) {
    ul,
    li,
    a {
        text-decoration: none;
        list-style: none;
    }

    .footer {
        width: 100vw;
        height: 20vh;
        background: linear-gradient(90deg, rgba(18, 21, 36, 1) 0%, rgba(36, 42, 66, 1) 50%, rgba(18, 21, 36, 1) 100%);
    }

    .wrap {
        width: 900px;
        margin: 0 auto;
        height: 100%;
    }

    .wrap__content {
        width: 100%;
        height: 90%;
        display: flex;
        align-items: center;
        justify-content: space-between;

    }

    .wrap-left {
        height: 100%;
        width: 76%;
        display: flex;
        align-items: center;
    }

    .wrap-left__logo {
        height: 100%;
        width: 25%;
        display: flex;
        align-items: center;
    }

    .wrap-left__text {
        font-size: 10px;
        color: #8a8d98;
        line-height: 25px;
    }

    .wrap-right {
        width: 21%;
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: space-evenly;
    }


    .footer__list {
        display: flex;
        align-items: center;
        justify-content: space-evenly;
    }

    .list__item {
        width: 100%;
    }

    .list__item-link {
        width: 100%;
    }

    .list__item-img {
        width: 70%;
    }

    .wrap-left__logo__link {
        width: 50%;
        height: 50%;
        display: flex;
        align-items: center;
    }

    .wrap-left__logo__link__img {
        width: 200%;
    }
}


@media screen and (max-width: 900px) {

    ul,
    li,
    a {
        text-decoration: none;
        list-style: none;
    }

    .footer {
        padding: 40px 0;
        width: 100vw;
        background: linear-gradient(90deg, rgba(18, 21, 36, 1) 0%, rgba(36, 42, 66, 1) 50%, rgba(18, 21, 36, 1) 100%);
    }

    .wrap {
        width: 300px;
        margin: 0 auto;
        height: 100%;
    }

    .wrap__content {
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: space-between;
        flex-direction: column;

    }

    .wrap-left {
        width: 100%;
        display: flex;
        align-items: center;
        flex-direction: column;
    }

    .wrap-left__logo {
        height: 100%;
        width: 70%;
        display: flex;
        align-items: center;
    }

    .wrap-left__text {
        text-align: center;
        font-size: 11px;
        color: #8a8d98;
        line-height: 25px;
        margin-top: 20px;
    }

    .wrap-right {
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: space-evenly;
        margin-top: 20px;
    }


    .footer__list {
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: space-evenly;
    }

    .list__item {
        width: 15%;
    }

    .list__item-link {
        width: 100%;
    }

    .list__item-img {
        width: 100%;
    }

    .wrap-left__logo__link {
        width: 50%;
        height: 50%;
        display: flex;
        align-items: center;
    }

    .wrap-left__logo__link__img {
        width: 200%;
    }

}
</style>



<script>

export default {
    data() {
        return {
            hrefs: [{
                id: 0,
                img: "/img/footer-YT.png",
                link: "https://www.youtube.com/OverwatchRU",
            },
            {
                id: 1,
                img: "/img/footer-reddit.png",
                link: "https://vk.com/overwatchru",
            },
            {
                id: 2,
                img: "/img/footer-vk.png",
                link: "https://vk.com/overwatchru",
            },
            ]
        }
    },
}

</script>
