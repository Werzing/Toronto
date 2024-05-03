<template>
    <div>

        <div class="bg" :style="{ backgroundImage: `url(/img/${bgdescription})` }">
            <slot name="description"></slot>
        </div>


        <div class="bg" :style="{ backgroundImage: `url(../img/${bg})` }">
            <slot name="skils"></slot>

        </div>
    </div>



</template>




<style>
* {
    color: white;
}

@media screen and (min-width: 1200px) {

    .bg {
        background-size: cover;
        background-position: center;
    }


}

@media screen and (max-width:1199px) and (min-width:901px) {
    .bg {
        background-size: cover;
        background-position-x: -900px;
    }
}

@media screen and (max-width:900px) {
    .bg {
        background-size: cover;
        background-position-x: -900px;
    }
}
</style>







<script>

export default {
    props: ["bgdescription", "bg"],

};

</script>