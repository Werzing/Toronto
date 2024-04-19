<template>
    <div class="swiper">
        <swiper :modules="modules" :slides-per-view="1" :space-between="0" navigation :pagination="{ clickable: true, }"
            :loop="true" :scrollbar="{ draggable: true }" :autoplay="{ delay: 8000, disableOnInteraction: true, }"
            @swiper="onSwiper" @slideChange="onSlideChange">

            <!--:pagination="{ clickable: true,dynamicBullets: true,} "-->

            <swiper-slide>
                <div class="slider">
                    <div class="slider__text">
                        <h3>ликвидация</h3>
                        <p>Устраните всех противников, чтобы одержать верх в раунде. Участвовать в боях могут команды из
                            одного, трех и шести игроков.</p>
                    </div>
                    <img src="/img/Black_Forest_Elimination.webp" alt="" class="slider__img">
                </div>
            </swiper-slide>

            <swiper-slide>
                <div class="slider">
                    <div class="slider__text">
                        <h3>Схватка</h3>
                        <p>Убивайте противников и наберите 20 очков в режиме «все против всех».</p>
                    </div>
                    <img src="/img/Eichenwalde_Deathmatch.webp" alt="" class="slider__img">
                </div>
            </swiper-slide>

            <swiper-slide>
                <div class="slider">
                    <div class="slider__text">
                        <h3>сопровождение</h3>
                        <p>Одна команда сопровождает груз до пункта назначения, а вторая пытается ей помешать.</p>
                    </div>
                    <img src="/img/Monte_Carlo_Escort.webp" alt="" class="slider__img">
                </div>
            </swiper-slide>

            <swiper-slide>
                <div class="slider">
                    <div class="slider__text">
                        <h3>Контроль</h3>
                        <p>Команды стараются захватить объект. В матче побеждает та команда, которая одержит верх в двух
                            раундах.</p>
                    </div>
                    <img src="/img/Oasis_Control.webp" alt="" class="slider__img">
                </div>
            </swiper-slide>

            <swiper-slide>
                <div class="slider">
                    <div class="slider__text">
                        <h3>«Точка возгорания»</h3>
                        <p>Команды сражаются на самых больших полях боя в игре, Нью-Джанке и Суравасе, за контроль над пятью
                            объектами. Бой идет до трех побед!</p>
                    </div>
                    <img src="/img/New_Junk_City_Flashpoint.webp" alt="" class="slider__img">
                </div>
            </swiper-slide>

            <swiper-slide>
                <div class="slider">
                    <div class="slider__text">
                        <h3>Захват флага</h3>
                        <p>Команды соревнуются, чтобы захватить вражеский флаг и защитить свой.</p>
                    </div>
                    <img src="/img/Lijang_Tower_Capture_the_Flag.webp" alt="" class="slider__img">
                </div>
            </swiper-slide>

            <swiper-slide>
                <div class="slider">
                    <div class="slider__text">
                        <h3>Гибридный режим</h3>
                        <p>Атакующая команда захватывает груз, а затем пытается доставить его в пункт назначения.
                            Обороняющаяся команда должна помешать ей это сделать.</p>
                    </div>
                    <img src="/img/Rio_de_Janeiro_Hybrid.webp" alt="" class="slider__img">
                </div>
            </swiper-slide>


            <swiper-slide>
                <div class="slider">
                    <div class="slider__text">
                        <h3>Натиск</h3>
                        <p>Устраните всех противников, чтобы одержать верх в раунде. Участвовать в боях могут команды из
                            одного, трех и шести игроков.</p>
                    </div>
                    <img src="/img/Toronto_Push.webp" alt="" class="slider__img">
                </div>
            </swiper-slide>


            <swiper-slide>
                <div class="slider">
                    <div class="slider__text">
                        <h3>Командная схватка</h3>
                        <p>Действуйте слаженно и обыграйте команду противника, совершив больше убийств.</p>
                    </div>
                    <img src="/img/Kanezaka_Team_Deathmatch.webp" alt="" class="slider__img">
                </div>
            </swiper-slide>

        </swiper>


    </div>
</template>




<script>
// import Swiper core and required modules
import { Navigation,A11y, Pagination} from 'swiper/modules';

// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';

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
            modules: [Navigation,Pagination,A11y],
        };
    },
};
</script>







<style scoped>
@media screen and (min-width: 1600px) {

.swiper{
    width: 100%; user-select: none;
}


.slider {
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    flex-direction: column-reverse;
    padding-top: 20px;
}

.slider__text {
    font-size: 19px;
    width: 90%;
    padding-bottom: 25px;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    text-align: center;
    flex-direction: column;
}

h3 {
    font-size: 20pt;
}

p{
    font-size: 14pt;
}

.slider__img {
    width: 92%;
}
}
</style>