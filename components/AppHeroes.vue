<template>
  <div class="wrap buttons heroeBG">

    <button class="buttons-filter" @click="getCountries()">Все герои</button>
    <button class="buttons-filter" @click="getDamage()">Урон</button>
    <button class="buttons-filter" @click="getTanks()">Танки</button>
    <button class="buttons-filter" @click="getSupports()">Поддержка</button>

    <div class="wrap cards">

      <NuxtLink class="heroe__card" :href="`/heroes/${heroe.id}`" v-for="heroe in heroes" :key="heroe.id">
        <div class="heroe__img"><img class="heroe__img" :src="`${heroe.NameImg}`" alt=""></div>
        <div class="heroe__description"><img class="roleImg" :src="`${heroe.RoleImg}`" alt=""> <span class="HeroeName">{{ heroe.name }}</span></div>

      </NuxtLink>


    </div>
  </div>



</template>



<style scoped>
@media screen and (min-width: 1200px) {

  .buttons-filter {
    padding: 15px;
    width: 12%;
    font-size: 16pt;
    border: 3px solid white;
    border-radius: 8px;
    background: linear-gradient(90deg, rgba(18, 21, 36, 1) 0%, rgba(36, 42, 66, 1) 50%, rgba(18, 21, 36, 1) 100%);
    cursor: pointer;
    transition: 0.2s;
    color: white;
  }

  .buttons-filter:hover {
    transform: scale(110%);

  }

  .cards {
    padding: 20px 0 50px 0;
  }

  .buttons {
    padding: 120px 0 20px 0;
  }

  .wrap {
    width: 1500px;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    gap: 40px;
  }

  .heroe__card {
    width: 14%;
    border: 4px solid white;
    border-radius: 10px;
    background: linear-gradient(90deg, rgba(18, 21, 36, 1) 0%, rgba(36, 42, 66, 1) 50%, rgba(18, 21, 36, 1) 100%);
    transition: 200ms;
    overflow: hidden;

  }


  .heroe__card:hover {

    transform: scale(110%);
  }


  .heroe__img {
    width: 100%;
  }

  .heroe__description {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    padding: 20px 0;
  }


  a,
  li,
  ul {
    list-style: none;
    text-decoration: none;
    color: white;
  }

}

@media screen and (max-width: 1199px) and (min-width:901px) {
  .roleImg {
    width: 20px;
  }


  .buttons-filter {
    padding: 15px;
    width: 15%;
    font-size: 10pt;
    border: 3px solid white;
    border-radius: 8px;
    background: linear-gradient(90deg, rgba(18, 21, 36, 1) 0%, rgba(36, 42, 66, 1) 50%, rgba(18, 21, 36, 1) 100%);
    cursor: pointer;
    transition: 0.2s;
    color: white;
  }

  .buttons-filter:hover {
    transform: scale(110%);

  }

  .cards {
    padding: 20px 0 50px 0;
  }

  .buttons {
    padding: 120px 0 20px 0;
  }

  .wrap {
    width: 910px;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    gap: 40px;
  }

  .heroe__card {
    width: 14%;
    border: 4px solid white;
    border-radius: 10px;
    background: linear-gradient(90deg, rgba(18, 21, 36, 1) 0%, rgba(36, 42, 66, 1) 50%, rgba(18, 21, 36, 1) 100%);
    transition: 200ms;
    overflow: hidden;

  }


  .heroe__card:hover {

    transform: scale(110%);
  }


  .heroe__img {
    width: 100%;
  }

  .heroe__description {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    padding: 20px 0;
  }


  a,
  li,
  ul {
    list-style: none;
    text-decoration: none;
    color: white;
  }
}

@media screen and (max-width: 900px) {

  .buttons-filter {
    padding: 15px;
    width: 40%;
    font-size: 8pt;
    border: 3px solid white;
    border-radius: 8px;
    background: linear-gradient(90deg, rgba(18, 21, 36, 1) 0%, rgba(36, 42, 66, 1) 50%, rgba(18, 21, 36, 1) 100%);
    cursor: pointer;
    transition: 0.2s;
    color: white;
  }



  .buttons {
    margin: 100px 0 0 0;
  }

  .wrap {
    width: 100vw;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    gap: 18px;
  }

  .heroe__card {
    width: 47%;
    border: 4px solid white;
    border-radius: 10px;
    background: linear-gradient(90deg, rgba(18, 21, 36, 1) 0%, rgba(36, 42, 66, 1) 50%, rgba(18, 21, 36, 1) 100%);
    transition: 200ms;
    overflow: hidden;

  }

  .heroe__img {
    width: 100%;
  }

  .heroe__description {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    padding: 20px 0;
  }


  a,
  li,
  ul {
    list-style: none;
    text-decoration: none;
    color: white;
  }

  .heroeBG {
    background: url(/img/heroeBG.jpg);
    background-size:cover;
    background-attachment: fixed;
    background-position-y: 120px;
    height: 90vh;
    padding: 90px 20px;
  }

}
</style>







<script setup>
import { createClient } from '@supabase/supabase-js'
const supabase = createClient('https://mvztgnwuhwrkolitusaz.supabase.co', 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6Im12enRnbnd1aHdya29saXR1c2F6Iiwicm9sZSI6ImFub24iLCJpYXQiOjE3MDA5MjUzMjIsImV4cCI6MjAxNjUwMTMyMn0.A36rKHamH50tWFTb0SLZwW7GhPB5rMiR5dup1rojMMY')
const heroes = ref([])



async function getCountries() {
  const { data } = await supabase.from('heroes').select().order("name", { ascending: true })
  heroes.value = data
}


async function getTanks() {
  const { data } = await supabase.from('heroes').select().order("name", { ascending: true }).eq("role", "Танк")
  heroes.value = data
}


async function getDamage() {
  const { data } = await supabase.from('heroes').select().order("name", { ascending: true }).eq("role", "Урон")
  heroes.value = data
}


async function getSupports() {
  const { data } = await supabase.from('heroes').select().order("name", { ascending: true }).eq("role", "Поддержка")
  heroes.value = data
}



onMounted(() => {
  getCountries()
})






</script>
