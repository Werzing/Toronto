<template>
    <div class="div-swiper">
        <swiper class="swiper" :modules="modules" :slides-per-view="1" :space-between="0" navigation
            :pagination="{ clickable: true, }" :loop="true" :scrollbar="{ draggable: true }" @swiper="onSwiper"
            @slideChange="onSlideChange" :autoplay="{ delay: 9000, disableOnInteraction: true, }">

            <!--:pagination="{ clickable: true,dynamicBullets: true,} "-->

            <swiper-slide class="slide">
                <div class="slider">
                    <div class="slider__text">
                        <h2>Танки</h2>
                        <p>Герои этой категории могут выдержать огромное количество урона и прорваться сквозь
                            укрепленные позиции, например, через большие группы героев вражеской команды или тесные
                            проходы. В роли танка вам предстоит вести за собой всю команду.</p>
                    </div>
                    <img src="/img/Tank_Heroes_Desktop.webp" alt="" class="slider__img">
                </div>
            </swiper-slide>

            <swiper-slide class="slide">
                <div class="slider">
                    <div class="slider__text">
                        <h2>Урон</h2>
                        <p>Герои этой категории призваны находить противников, навязывать им бой и устранять их,
                            используя свои умения и способности. Они способны нанести серьезный ущерб команде
                            противника, но при этом весьма уязвимы, и поэтому нуждаются в помощи союзников.</p>
                    </div>
                    <img src="/img/Damage_Heroes_Desktop.webp" alt="" class="slider__img">
                </div>
            </swiper-slide>

            <swiper-slide class="slide">
                <div class="slider">
                    <div class="slider__text">
                        <h2>Поддержка</h2>
                        <p>Герои этой категории усиливают союзников, исцеляют и укрывают их щитами, а также нейтрализуют
                            противников. В роли героя поддержки вы отвечаете за выживание вашей команды.</p>
                    </div>
                    <img src="/img/Support_Heroes_Desktop.webp" alt="" class="slider__img">
                </div>
            </swiper-slide>


        </swiper>


    </div>
</template>




<script>
// import Swiper core and required modules
import { Navigation, A11y, Autoplay } from 'swiper/modules';

// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/autoplay';

// Import Swiper styles
export default {
    components: {
        Swiper,
        SwiperSlide,
    },
    setup() {
        const onSwiper = (swiper) => {
            console.log(swiper);
        };
        const onSlideChange = () => {
            console.log('slide change');
        };
        return {
            onSwiper,
            onSlideChange,
            modules: [Navigation, A11y, Autoplay],
        };
    },
};
</script>






<style scoped>
@media screen and (min-width: 1600px) {

.div-swiper {
    width: 90%;
    height: 100%;
    user-select: none;
}

.swiper {
    width: 100%;
    height: 100%;
}

.slider {
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    flex-direction: row-reverse;
    margin-top: 40px;
    background-color: rgba(0, 0, 0, 0.534);
    border-radius: 14px;
}

h2 {
    font-size: 20pt;
    width: 100%;
    padding-bottom: 20px;
}

p {
    font-size: 14pt;
}

.slider__text {
    width: 50%;
    height: 50%;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    text-align: left;
    flex-direction: column;
    line-height: 25px
}

.slider__img {
    width: 35%;
    height: 75%;
}

}


@media screen and (max-width: 900px) {

.div-swiper {
    width: 90%;
    height: 100%;
    user-select: none;
}

.swiper {
    width: 100%;
    height: 100%;
}

.slider {
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    flex-direction: row-reverse;
    margin-top: 40px;
    background-color: rgba(0, 0, 0, 0.534);
    border-radius: 14px;
}

h2 {
    font-size: 20pt;
    width: 100%;
    padding-bottom: 20px;
}

p {
    font-size: 14pt;
}

.slider__text {
    width: 50%;
    height: 50%;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    text-align: left;
    flex-direction: column;
    line-height: 25px
}

.slider__img {
    width: 35%;
    height: 75%;
}

}

</style>