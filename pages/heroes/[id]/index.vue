<template>

  <div style="z-index: -9999999999999999999; width: 100vw; height: 100vh;    background: linear-gradient(90deg, rgba(18, 21, 36, 1) 0%, rgba(36, 42, 66, 1) 50%, rgba(18, 21, 36, 1) 100%);
 position: absolute; display: flex; align-items: center; justify-content: center;">

    <img src="/video/cat.gif" alt="" style="width: 70px; height: 70px;">
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




  <div v-if="heroe">

    <AppHeroesDescription :bgdescription="`heroesBG/1600_${heroe.id}.jpg`" :bg="`heroesBG/${heroe.id}.jpg`">



      <template v-slot:description>

        <div
          style="display: flex; align-items: start; justify-content: center; flex-direction: column; padding: 280px 100px">
          <div style="width: 50%;">
            <h2 style="display: flex; align-items: center; font-size: 35px; margin-bottom:20px; ">
              {{ heroe.name }}
            </h2>

            <p style=" line-height: 35px; margin: 30px 0">
              {{ heroe.name }} — {{ heroe.description }}</p>
          </div>
          <h3 style="display: flex; align-items: center;">
            Роль:
            {{ heroe.role }}
            <img style="padding: 20px; width: 70px;" :src="`${heroe.RoleImg}`" alt="">
          </h3>

          <h3>
            Здоровье: {{ heroe.health }}

          </h3>

        </div>
      </template>




      <template v-slot:skils>
        <div
          style="width: 100vw;  display: flex; align-items: center; justify-content: center; flex-direction: column; padding: 100px 0">
          <h2 style="margin-bottom: 60px;">Способности</h2>

          <img style="width: 80%; border: 4px solid white; border-radius:10px; text-align: center;"
            :src="`/img/heroes/${heroe.name}.png`" :alt="`Описание способностей: ${heroe.name}`">
        </div>
      </template>
    </AppHeroesDescription>


    
    <AppFooter />

  </div>



  <div v-else style="width: 100vw; height: 100vh; display: flex; align-items: end;">
    <AppFooter />

  </div>
</template>




<style scoped>

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

nav a {
    text-decoration: none;
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


    }
  },



}


</script>


<script setup>


import { createClient } from '@supabase/supabase-js'
const supabase = createClient('https://mvztgnwuhwrkolitusaz.supabase.co', 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6Im12enRnbnd1aHdya29saXR1c2F6Iiwicm9sZSI6ImFub24iLCJpYXQiOjE3MDA5MjUzMjIsImV4cCI6MjAxNjUwMTMyMn0.A36rKHamH50tWFTb0SLZwW7GhPB5rMiR5dup1rojMMY')
const heroe = ref()
const route = useRoute()



async function getCountries() {
  const { data } = await supabase.from('heroes').select().eq("id", `${route.params.id}`).single()
  heroe.value = data
  console.log(data);
}

onMounted(() => {
  getCountries()
  
})

</script>
