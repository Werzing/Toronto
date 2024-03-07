<template>

<app-header>

      
<template v-slot:vidioBg>
  <video class="vidioBg" src="/video/F2P_Trailer.mp4"
      poster="/img/HeaderBG4.jpg"
       muted></video>
</template>


</app-header>



  <AppBackground :bg="'normBG5.jpg'">

    <template v-slot:top>
      <app-heroes />
    </template>

  </AppBackground>




 <AppFooter/>
</template>