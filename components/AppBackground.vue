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
</style>


<script>

export default {
    props: ['bg']
}

</script>


