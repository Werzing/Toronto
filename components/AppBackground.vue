<template>
    <div class="bg" :style="{ backgroundImage: `url(/img/${bg})` }">
        <div class="darkeningOfTheBackground">
            <div>
                <slot name="top"></slot>
            </div>
        </div>

    </div>
</template>


<style scoped>
*{
    color: white;
}

@media screen and (min-width: 1200px) {

.darkeningOfTheBackground {
    height: 100%;
    width: 100%;
    background-color: #02023b36;
}

.bg{
    background-size: cover; 
    background-position: center; 
    background-attachment: fixed;
}

}

@media  screen and (max-width:1199px) and (min-width: 901px) {
    
}

@media screen and (max-width: 900px) {

.darkeningOfTheBackground {
    text-align: center;
    background-color: #02023b36;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.bg{
    background-size: cover; 
    background-position: center; 
}

}
</style>


<script>

export default {
    props: ['bg']
}

</script>


