<template>
    <div class="content">
        <div class="matte" :style="{ backgroundImage: `url(/img/${bg})` }">
            <div class="wrap">
                <div class="wrap__content">
                    <slot name="img"></slot>


                    <slot name="text"></slot>
                </div>

                <div class="wrap__content2">
                    <slot name="video"></slot>
                    <slot name="video-text"></slot>

                </div>
            </div>
        </div>





    </div>
</template>


<style scoped>
* {
    color: white;
}

@media screen and (min-width: 1600px) {

    .wrap__content2 {
        display: flex;
        align-items: center;
        justify-content: space-between;
        flex-direction: row-reverse;
        width: 100%;
        height: 100%;
    }



    .content {
        width: 100vw;
        position: relative;
    }


    .wrap {
        width: 1700px;
        margin: 0 auto;
        padding: 100px 0;
    }

    .wrap__content {
        display: flex;
        align-items: center;
        justify-content: space-between;
        line-height: 32px;
        width: 100%;
    }


    .matte {
        width: 100%;
        background-size: cover;
        position: relative;
        background-position-y: center;
        z-index: 10;
        display: flex;
        align-items: center;
        overflow: hidden;
        padding: 40px 0;
    }



    .matte:before {
        position: absolute;
        content: '';
        background: inherit;
        left: -1px;
        right: 0px;
        top: 0px;
        bottom: 0;
        filter: blur(15px);
        border-radius: 15px;
        z-index: -1;
    }

}



@media screen and (max-width: 900px) {

    .wrap__content2 {
        display: flex;
        align-items: center;
        justify-content: space-between;
        flex-direction: column-reverse;
        width: 100%;
        text-align: center;
    }



    .content {
        width: 100vw;
        position: relative;
    }


    .wrap {
        width: 350px;
        padding: 80px 0;
        margin: 0 auto;
    }

    .wrap__content {
        text-align: center;
        display: flex;
        align-items: center;
        justify-content: space-between;
        flex-direction: column-reverse;
        line-height: 32px;
        width: 100%;
    }


    .matte {
        width: 100%;
        background-size: cover;
        position: relative;
        background-position: center;
        z-index: 10;
        display: flex;
        align-items: center;
        overflow: hidden;
        padding: 40px 0;
    }



    .matte:before {
        position: absolute;
        content: '';
        background: inherit;
        left: -1px;
        right: 0px;
        top: 0px;
        bottom: 0;
        filter: blur(15px);
        border-radius: 15px;
        z-index: -1;
    }

}
</style>



<script>
export default {
    props: ['bg']
}

</script>