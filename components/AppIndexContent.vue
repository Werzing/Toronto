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

@media screen and (min-width: 1200px) {

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


@media screen and (max-width: 1199px) and (min-width:901px) {
    .wrap__content2 {
        display: flex;
        align-items: center;
        justify-content: space-between;
        flex-direction: column;
        width: 100%;
        height: 100%;
    }



    .content {
        width: 100vw;
        position: relative;
    }


    .wrap {
        width: 900px;
        margin: 0 auto;
        padding: 100px 0;
    }

    .wrap__content {
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
        flex-direction: column-reverse;
        background: linear-gradient(90deg, rgba(18, 21, 36, 0.384) 0%, rgba(36, 42, 66, 0.384) 50%, rgba(18, 21, 36, 0.384) 100%), url(/img/wrap__content2.jpg);
        text-align: center;
        line-height: 26px;
    }



    .content {
        width: 100vw;
        position: relative;
    }


    .wrap {
        width: 100%;
    }

    .wrap__content {
        display: flex;
        flex-direction: column-reverse;
        background: linear-gradient(90deg, rgba(18, 21, 36, 0.384) 0%, rgba(36, 42, 66, 0.384) 50%, rgba(18, 21, 36, 0.384) 100%), url(/img/wrap__content.jpg);
        text-align: center;
        line-height: 26px;
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