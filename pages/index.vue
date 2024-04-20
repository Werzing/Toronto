<template>
  <div>
    <app-header>


      <template v-slot:vidioBg>
        <video class="vidioBg" src="/video/F2P_Trailer.mp4" poster="/img/Lijang_Tower_Capture_the_Flag.webp"  muted autoplay></video>
      </template>


    </app-header>



    <AppIndexContent :bg="'HeaderBG3.jpeg'">

      <template v-slot:img>
        <video class="video" poster="/img/BgForVideo.webp" src="/video/Overwatch 2 _ Season9.mp4" controls></video>
      </template>

      <template v-slot:text>
        <div class="seson9-text">
          <h3 class="index__text-h3">ОБНОВЛЕННАЯ СОРЕВНОВАТЕЛЬНАЯ ИГРА</h3>
          <p class="index__text-p">Пришло время занять свое место в рейтинге полностью обновленной соревновательной
            игры:
            теперь система стала
            понятнее, ранг обновляется в реальном времени и более точно отражает ваши навыки. Вы сможете получить новые
            нефритовые варианты оружия и подняться до «Чемпиона» — нового престижного ранга, который на ступень выше
            ранга
            «Элита».</p>
        </div>
      </template>

    </AppIndexContent>



    <AppBackground :bg="'section3.jpg'" id="modes">

      <template v-slot:top>

        <div class="wrap2">
          <div class="section3">
            <div class="section3__text">
              <h3 class="bg__text-h3">Режимы игры</h3>
              <p class="bg__text-p">Сражайтесь за будущее в самых разных уголках мира. На каждом из
                полей боя — от полного высокотехнологичных
                чудес Пусана до заснеженных улиц Торонто — вас ждут задачи, тайны и стратегические возможности.</p>
            </div>

            <AppSliderIndexOne></AppSliderIndexOne>

          </div>

        </div>
      </template>

    </AppBackground>



    <AppIndexContent :bg="'14-min.jpg'">

      <template v-slot:video>
        <video class="video" poster="/img/promo-poster.jpg" src="/video/Promo.mp4" controls></video>
      </template>

      <template v-slot:video-text>
        <div class="seson9-text">
          <h3 class="index__text-h3">Держитесь вместе!</h3>
          <p class="index__text-p">Уинстон собирает небольшой ударный отряд, чтобы отбить внезапное нападение
            «Нуль-сектора» на одну из столиц. И когда надежда начинает таять, команде героев приходится собрать все
            силы, чтобы сделать невозможное.</p>

        </div>

      </template>

    </AppIndexContent>



    <AppBackground :bg="'section2.jpg'" id="role">

      <template v-slot:top>
        <div class="wrap2">
          <div class="section2">
            <div>
              <h3 class="bg__text-h3">Классы</h3>

            </div>
            <AppSliderIndexTwo></AppSliderIndexTwo>
          </div>
        </div>

      </template>

    </AppBackground>



    <AppFooter />
  </div>
</template>



<style>
@media screen and (min-width: 1600px) {

  .vidioBg {
    width: 100%;
  }

  .video {
    width: 50%;
    border-radius: 30px;
    border: 4px solid rgb(190, 190, 190);
  }

  .wrap2 {
    width: 1200px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
  }

  .seson9-text {
    height: 400px;
    display: flex;
    justify-content: space-evenly;
    flex-direction: column;
    width: 45%;
  }


  .index__text-h3 {
    line-height: 32px;
    font-size: 20pt;
  }

  .index__text-p {
    line-height: 32px;
    font-size: 14pt;
  }


  .bg__text-h3 {
    line-height: 32px;
    font-size: 25pt;
  }

  .bg__text-p {
    line-height: 32px;
    font-size: 14pt;
  }


  .section3 {
    z-index: 999;
    text-align: center;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    flex-direction: column;
    width: 80%;
    height: 100%;
    padding: 120px 0;
  }

  .section3__text {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-direction: column;
  }




  .section2 {
    z-index: 999;
    text-align: center;
    display: flex;
    align-items: center;
    justify-content: space-around;
    flex-direction: column;
    width: 100%;
    padding: 120px 0;
  }
}

@media screen and (max-width: 900px) {

  .video {
    width: 100%;
    margin-top: 60px;
    border-radius: 10px;
    border: 2px solid white;
  }

  .section2{
    padding: 35px 0;
  }

  .section3{
    padding: 35px 0;
  }

}
</style>
