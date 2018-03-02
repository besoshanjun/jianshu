<template>
    <div>
        <my-header></my-header>
        <div class="index my-container">
            <div class="row">
                <div class="col-8 main">
                    <!--轮播图-->
                    <div v-swiper:mySwiper="swiperOption" class="banner">
                        <div class="swiper-wrapper">
                            <div class="swiper-slide" v-for="banner in banners">
                                <img :src="banner">
                            </div>
                        </div>
                        <div class="swiper-pagination swiper-pagination-white"></div>
                        <div class="swiper-button-next swiper-button-white"></div>
                        <div class="swiper-button-prev swiper-button-white"></div>
                    </div>
                    <!--推荐专题-->
                    <div class="recommend-collection">
                        <nuxt-link to="/">
                            <img src="../assets/img/z-1.png">
                            <span>旅行·在路上</span>
                        </nuxt-link>
                        <nuxt-link to="/">
                            <img src="../assets/img/z-2.jpg">
                            <span>故事</span>
                        </nuxt-link>
                        <nuxt-link to="/">
                            <img src="../assets/img/z-3.jpg">
                            <span>人文社科</span>
                        </nuxt-link>
                        <nuxt-link to="/">
                            <img src="../assets/img/z-1.png">
                            <span>旅行·在路上</span>
                        </nuxt-link>
                        <nuxt-link to="/">
                            <img src="../assets/img/z-2.jpg">
                            <span>@IT·互联网</span>
                        </nuxt-link>
                        <nuxt-link to="/">
                            <img src="../assets/img/z-3.jpg">
                            <span>人文社科</span>
                        </nuxt-link>
                        <nuxt-link to="/">
                            <img src="../assets/img/z-2.jpg">
                            <span>社会热点</span>
                        </nuxt-link>
                        <nuxt-link to="/recommendations" class="more-hot-collection">
                            更多热门专题
                            <i class="fa fa-chevron-right"></i>
                        </nuxt-link>
                    </div>
                    <div class="split-line"></div>
                    <!--文章列表-->
                    <div id="list-container">
                        <ul class="note-list">
                            <li class="have-img">
                                <nuxt-link class="wrap-img" to="/p/123">
                                    <img src="../assets/img/pic-1.jpg">
                                </nuxt-link>
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="/u/123" class="avatar">
                                            <img src="../assets/img/user.jpg" alt="">
                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="/u/123" class="nickname">萌薇</nuxt-link>
                                            <span class="time">8小时前</span>
                                        </div>
                                    </div>
                                    <nuxt-link class="title" to="/p/123">
                                        如何把书中的知识转化成能力？这是我见过的最好回答
                                    </nuxt-link>
                                    <p class="abstract">
                                        随着知识经济的兴起，读书的重要性得到了大家的普遍认同，于是市场上出现很多读书方法，比如速度、多读、慢读、列读……不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
                                    </p>
                                    <div class="meta">
                                        <nuxt-link to="/collection/123" class="collection-tag">
                                            读书
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="p/123">
                                            <i class="fa fa-eye"></i>
                                            12054
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="/p/123">
                                            <i class="fa fa-comment"></i>
                                            96
                                        </nuxt-link>
                                        <span>
                                            <i class="fa fa-heart"></i>
                                            800
                                        </span>
                                    </div>
                                </div>
                            </li>
                            <li>
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="/u/123" class="avatar">
                                            <img src="../assets/img/user.jpg" alt="">
                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="/u/123" class="nickname">萌薇</nuxt-link>
                                            <span class="time">8小时前</span>
                                        </div>
                                    </div>
                                    <nuxt-link class="title" to="/p/123">
                                        如何把书中的知识转化成能力？这是我见过的最好回答
                                    </nuxt-link>
                                    <p class="abstract">
                                        随着知识经济的兴起，读书的重要性得到了大家的普遍认同，于是市场上出现很多读书方法，比如速度、多读、慢读、列读……不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
                                    </p>
                                    <div class="meta">
                                        <nuxt-link to="/collection/123" class="collection-tag">
                                            读书
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="p/123">
                                            <i class="fa fa-eye"></i>
                                            12054
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="/p/123">
                                            <i class="fa fa-comment"></i>
                                            96
                                        </nuxt-link>
                                        <span>
                                            <i class="fa fa-heart"></i>
                                            800
                                        </span>
                                    </div>
                                </div>
                            </li>
                            <li class="have-img">
                                <nuxt-link class="wrap-img" to="/p/123">
                                    <img src="../assets/img/pic-1.jpg">
                                </nuxt-link>
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="/u/123" class="avatar">
                                            <img src="../assets/img/user.jpg" alt="">
                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="/u/123" class="nickname">萌薇</nuxt-link>
                                            <span class="time">8小时前</span>
                                        </div>
                                    </div>
                                    <nuxt-link class="title" to="/p/123">
                                        如何把书中的知识转化成能力？这是我见过的最好回答
                                    </nuxt-link>
                                    <p class="abstract">
                                        随着知识经济的兴起，读书的重要性得到了大家的普遍认同，于是市场上出现很多读书方法，比如速度、多读、慢读、列读……不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
                                    </p>
                                    <div class="meta">
                                        <nuxt-link to="/collection/123" class="collection-tag">
                                            读书
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="p/123">
                                            <i class="fa fa-eye"></i>
                                            12054
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="/p/123">
                                            <i class="fa fa-comment"></i>
                                            96
                                        </nuxt-link>
                                        <span>
                                            <i class="fa fa-heart"></i>
                                            800
                                        </span>
                                    </div>
                                </div>
                            </li>
                            <li>
                                <div class="content">
                                    <div class="author">
                                        <nuxt-link to="/u/123" class="avatar">
                                            <img src="../assets/img/user.jpg" alt="">
                                        </nuxt-link>
                                        <div class="info">
                                            <nuxt-link to="/u/123" class="nickname">萌薇</nuxt-link>
                                            <span class="time">8小时前</span>
                                        </div>
                                    </div>
                                    <nuxt-link class="title" to="/p/123">
                                        如何把书中的知识转化成能力？这是我见过的最好回答
                                    </nuxt-link>
                                    <p class="abstract">
                                        随着知识经济的兴起，读书的重要性得到了大家的普遍认同，于是市场上出现很多读书方法，比如速度、多读、慢读、列读……不管你采用哪一种读书方法，最终都要回归到“行动”二字上，正如陆...
                                    </p>
                                    <div class="meta">
                                        <nuxt-link to="/collection/123" class="collection-tag">
                                            读书
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="p/123">
                                            <i class="fa fa-eye"></i>
                                            12054
                                        </nuxt-link>
                                        <nuxt-link class="tag" to="/p/123">
                                            <i class="fa fa-comment"></i>
                                            96
                                        </nuxt-link>
                                        <span>
                                            <i class="fa fa-heart"></i>
                                            800
                                        </span>
                                    </div>
                                </div>
                            </li>
                        </ul>
                    </div>
                    <!--阅读更多-->
                    <nuxt-link to="/" class="load-more">阅读更多</nuxt-link>
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
                    <div class="download">
                        <img src="../assets/img/zs.jpg">
                    </div>
                    <div class="recommend-author">
                        <div class="title">
                            <span>推荐作者</span>
                            <a href="javascript:void(0)" class="page-change" @click="rotate">
                                <i ref="refresh" class="fa fa-refresh"></i>
                                换一批
                            </a>
                        </div>
                        <ul class="list">
                            <li>
                                <nuxt-link class="avatar" to="/u/123">
                                    <img src="../assets/img/user.jpg">
                                </nuxt-link>
                                <nuxt-link class="follow" to="/u/123">
                                    <i class="fa fa-plus-square-o"></i>
                                    关注
                                </nuxt-link>
                                <nuxt-link class="name" to="/u/123">
                                    占小狼
                                </nuxt-link>
                                <p>
                                    写了152.9k·7.2k喜欢
                                </p>
                            </li>
                            <li>
                                <nuxt-link class="avatar" to="/u/123">
                                    <img src="../assets/img/user.jpg">
                                </nuxt-link>
                                <nuxt-link class="follow" to="/u/123">
                                    <i class="fa fa-plus-square-o"></i>
                                    关注
                                </nuxt-link>
                                <nuxt-link class="name" to="/u/123">
                                    占小狼
                                </nuxt-link>
                                <p>
                                    写了152.9k·7.2k喜欢
                                </p>
                            </li>
                            <li>
                                <nuxt-link class="avatar" to="/u/123">
                                    <img src="../assets/img/user.jpg">
                                </nuxt-link>
                                <nuxt-link class="follow" to="/u/123">
                                    <i class="fa fa-plus-square-o"></i>
                                    关注
                                </nuxt-link>
                                <nuxt-link class="name" to="/u/123">
                                    占小狼
                                </nuxt-link>
                                <p>
                                    写了152.9k·7.2k喜欢
                                </p>
                            </li>
                        </ul>
                        <nuxt-link to="/recommendations" class="find-more">
                            查看全部
                            <i class="fa fa-angle-right"></i>
                        </nuxt-link>
                    </div>
                </div>
            </div>
        </div>
        <footer class="my-container">
            <div class="row">
                <div class="col-9">
                   <ul class="list">
                       <li>关于简书&nbsp;·&nbsp;</li>
                       <li>联系我们&nbsp;·&nbsp;</li>
                       <li>加入我们&nbsp;·&nbsp;</li>
                       <li>简书出版&nbsp;·&nbsp;</li>
                       <li>品牌与徽标&nbsp;·&nbsp;</li>
                       <li>帮助中心&nbsp;·&nbsp;</li>
                       <li>合作伙伴</li>
                   </ul>
                    <div class="jiesao">
                        ©2012-2018 上海佰集信息科技有限公司 / 简书 / 沪ICP备11018329号-5 / &x3000:;
                        <img src="../assets/img/sm.png">
                        沪公网安备31010402002252号 /
                        <img src="../assets/img/phone.png">
                        举报电话：021-34770013 /
                        <img src="../assets/img/zz.png">
                    </div>
                </div>
            </div>
        </footer>
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
                    autoplay: {
                        delay: 3000,//切换时间
                        stopOnlastSlide: false,//是否停止在最后一张
                        disableOnOnteraction: false//禁止轮播
                    },
                    pagination: {
                        el: '.swiper-pagination'
                    },
                    navigation: {
                        nextEl: '.swiper-button-next',
                        prevEl: '.swiper-button-prev',
                    }
                },
                deg:0
            }
        },
        components: {
            myHeader
        },
        mouted(){

        },
        methods:{
            rotate:function () {
                this.deg = this.deg + 360
                let deg = this.$refs.refresh.style
                this.$refs.refresh.style.transform = `rotate(${this.deg}deg)`;
            }
        }
    }
</script>
<style>
    .swiper-button-next {
        background-color: rgba(0, 0, 0, 0.4);
    }

    .swiper-button-prev {
        background-color: rgba(0, 0, 0, 0.4);
    }
</style>
