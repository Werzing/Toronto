<template>

  <div class="preloader" style="width: 100vw;
  height: 100vh;
  background: linear-gradient(90deg, rgba(18, 21, 36, 1) 0%, rgba(36, 42, 66, 1) 50%, rgba(18, 21, 36, 1) 100%);
  position: absolute;
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: -999999999999999999;">

    <img src="/video/cat.gif" alt="" class="preloader__cat">
  </div>


  <nav class="navbar_scrolled nav">
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

    <a href="https://store.steampowered.com/app/2357570/Overwatch_2/"><button class="play">Играть</button></a>

  </nav>


  <div v-if="show" class="preloader__footer">

    <AppFooter />
  </div>


  <div v-else>
    <AppBackground :bg="'normBG5.jpg'">

      <template v-slot:top>
        <app-heroes />
      </template>

    </AppBackground>

    <AppFooter />
  </div>

</template>



<style scoped>


@media screen and (min-width: 1600px) {
  
nav a {
  text-decoration: none;
  color: white;
}



.preloader__cat {
  width: 70px;
  height: 70px;

}

.preloader__footer {
  width: 100vw;
  height: 100vh;
  display: flex;
  align-items: flex-end;
}

.play {
  padding: 13px 25px;
  background-color: #ff6400;
  color: white;
  border: none;
  border-radius: 2px;
  font-size: 12pt;
  cursor: pointer;
  transition: 200ms;
}

.play:hover {
  transform: scale(110%);
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

}

@media screen and (max-width: 900px) {
  
  .nav {
        width: 90%;
        margin: 0 auto;
        height: 20%;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    .nav__list {
        list-style: none;
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
    }

    .list__item{
        padding: 3px 0;
    }


    a{
        text-decoration: none;
    }

    .play {
        background-color: #ff6400;
        border: none;
        padding: 10px 15px;
        border-radius: 4px;
    }

    .logo-logo {
        width: 90%;
    }
}
</style>





<script>

export default {
  data() {
    return {
      show: true,
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


    }
  },
  mounted() {
    document.title = "Герои"
    this.showToggle()
  },

  methods: {
    showToggle() {
      setTimeout(() => {
        this.show = false
      }, 650)
    }

  }



}


</script>
