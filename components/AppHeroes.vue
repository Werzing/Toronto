<template>

  <div class="wrap">

    <NuxtLink class="heroe__card" :href="`/heroes/${heroe.id}`" v-for="heroe in heroes" :key="heroe.id">
        <div class="heroe__img"><img :src="`${heroe.NameImg}`" alt=""></div>
        <div class="heroe__description" ><img :src="`${heroe.RoleImg}`" alt=""> {{ heroe.name }}</div>

    </NuxtLink>
  </div>

</template>



<style scoped>
.wrap {
  width: 1700px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
  padding: 90px 0;
  gap: 40px;
}

.heroe__card{
  width: 14%;
  border: 4px solid white;
  border-radius: 5px;
  background: linear-gradient(90deg, rgba(18, 21, 36, 1) 0%, rgba(36, 42, 66, 1) 50%, rgba(18, 21, 36, 1) 100%);
  transition: 200ms;
  overflow: hidden;

}


.heroe__card:hover{

  transform: scale(110%);
}


.heroe__img{
  width: 100%;
}

.heroe__description{
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  padding: 20px 0;
}


a, li, ul{
  list-style: none;
  text-decoration: none;
  color: white;
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

onMounted(() => {
  getCountries()
})
</script>
