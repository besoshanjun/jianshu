<template>
    <div>
        <my-header></my-header>
        <div class="index my-container">
            <div class="row">
                <div class="col-8 main">
                    <!--<div class="banner">-->
                        <div v-swiper:mySwiper="swiperOption"  class="banner">
                            <div class="swiper-wrapper">
                                <div class="swiper-slide" v-for="banner in banners">
                                    <img :src="banner">
                                </div>
                            </div>
                            <div class="swiper-pagination swiper-pagination-white"></div>
                            <div class="swiper-button-next swiper-button-white"></div>
                            <div class="swiper-button-prev swiper-button-white"></div>
                        </div>
                    <!--</div>-->
                </div>
                <div class="col-4 aside">
                    <div class="board">
                        <nuxt-link to=".">
                            <img src="../assets/img/right-1.png">
                        </nuxt-link>
                        <nuxt-link to=".">
                            <img src="../assets/img/right-2.png">
                        </nuxt-link>
                        <nuxt-link to=".">
                            <img src="../assets/img/right-3.png">
                        </nuxt-link>
                        <nuxt-link to=".">
                            <img src="../assets/img/right-4.png">
                        </nuxt-link>
                        <nuxt-link to=".">
                            <img src="../assets/img/right-5.png">
                        </nuxt-link>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    import myHeader from '~/components/myHeader'
    export default{
        data(){
            return {
                banners: [
                    '/lunbo-1.jpg',
                    '/lunbo-2.jpg',
                    '/lunbo-3.jpg',
                    '/lunbo-4.jpg'
                ],
                swiperOption: {
                    loop: true,
                    slidesPerView: 'auto',
                    centeredSlides: true,
                    spaceBetween: 30,
                    autoplay:{
                        delay:3000,//切换时间
//                        stopOnlastSlide:false,//是否停止在最后一张
                        disableOnOnteraction:false//禁止轮播
                    },
                    pagination: {
                        el: '.swiper-pagination'
                    },
                    navigation:{
                        nextEl:'.swiper-button-next',
                        prevEl:'.swiper-button-prev',
                    }
                }
            }
        },
        components: {
            myHeader
        }
    }
</script>
<style>
    .swiper-button-next{
        background-color: rgba(0,0,0,0.4);
    }
    .swiper-button-prev{
        background-color: rgba(0,0,0,0.4);
    }
</style>
