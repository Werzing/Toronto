<template>
  <div>
      <NuxtPage />
  </div>
</template>



<style>
@font-face {
  font-family:"intro";
  src: url(assets/fonts/intro.otf);
}

*{
  margin: 0;
  padding: 0;
  font-family: "intro";
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


