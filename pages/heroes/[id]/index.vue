<template>
  <app-header>


    <template v-slot:vidioBg>
      <video class="vidioBg" src="/video/F2P_Trailer.mp4" poster="/img/HeaderBG4.jpg" muted></video>
    </template>


  </app-header>




  <AppBackground :bg="'normBG5.jpg'">

    <template v-slot:top>
      <div v-if="heroe">
        

        




      </div>
    </template>

  </AppBackground>

  <AppFooter />
</template>




<style></style>







































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
