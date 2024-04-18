<template>
    <div>

        <div class="bg" :style="{ backgroundImage: `url(/img/${bgdescription})` }">
            <slot name="description"></slot>
        </div>


        <div class="bg" :style="{backgroundImage: `url(../img/${bg})`}">
            <slot name="skils"></slot>

        </div>
    </div>



</template>




<style>
.bg{
    background-size: cover; 
    background-position: center; 
}

*{
    color:white;
}

</style>







<script>

export default {
    props: ["bgdescription","bg"],

};

</script>