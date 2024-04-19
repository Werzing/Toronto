<template>
  <div>
      <NuxtPage />
  </div>
</template>



<style>
@font-face {
  font-family:"intro";
  src: url(assets/fonts/Intro.otf);
}

body{
  background: linear-gradient(90deg, rgba(18, 21, 36, 1) 0%, rgba(36, 42, 66, 1) 50%, rgba(18, 21, 36, 1) 100%);
}

*{
  margin: 0;
  padding: 0;
  font-family: 'intro';
  text-shadow: 1px 2px 2px rgb(0, 0, 0);
  box-sizing: border-box;
}

body{
  overflow-x: clip;
}

body::-webkit-scrollbar{
  width: 14px;
}

body::-webkit-scrollbar-track{
  background: rgb(136, 136, 136);
}

body::-webkit-scrollbar-thumb{
  background-color:#ff6400;
  border-radius: 20px;
}
</style>


