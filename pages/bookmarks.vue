<template>
    <div>
        <my-header></my-header>
        <div class="bookmarks my-container">
            <div class="row">
                <div class="col-9 main" style="margin-left:12.5%">
                    <img class="tag-banner" src="../assets/img/bookmarks.png">
                    <!--文章列表模块-->
                    <ul class="note-list">
                        <li class="have-img">
                            <a href="javascript:void(0)" class="wrap-img">
                                <img class="img-blur-done" src="~assets/img/ceshi1.jpg">
                            </a>
                            <div class="content" @mouseover="showCancel=true" @mouseleave="showCancel=false">
                                <div class="author">
                                    <a href="javascript:void(0)" class="avatar">
                                        <img src="~assets/img/user.jpg">
                                    </a>
                                    <div class="info">
                                        <a class="nickname" href="javascript:void(0)">可可西里里</a>
                                        <a href="javascript:void(0)">
                                            <img class="badge-icon" src="~assets/img/ceshi3.png">
                                        </a>
                                        <span class="time">02.33  15:48</span>
                                    </div>
                                </div>
                                <a class="title" href="javascript:void(0)">
                                    女生都爱的仙女裙怎么穿？
                                </a>
                                <p class="abstract">

                                    文/可可西里里   今天的着装话题说说仙女裙--仙女裙的特点：飘逸柔美，常用的布料是网纱、雪纺、蕾丝等面料.有些美女可能要说仙女裙太薄了，要夏天穿才对--如果这样想那您就奥特...

                                </p>
                                <div class="meta">
                                    <a href="javascript:void(0)">
                                        <i class="fa fa-eye"></i>
                                        4899
                                    </a>
                                    <a href="javascript:void(0)">
                                        <i class="fa fa-comment"></i>
                                        37
                                    </a>
                                    <span>
                                        <i class="fa fa-heart"></i>
                                        45
                                    </span>
                                    <a v-show="showCancel" class="cancel" href="javascript:void(0)">取消关注</a>
                                </div>
                            </div>
                        </li>
                        <li class="have-img">
                            <a href="javascript:void(0)" class="wrap-img">
                                <img class="img-blur-done" src="~assets/img/ceshi1.jpg">
                            </a>
                            <div class="content" @mouseover="showCancel=true" @mouseleave="showCancel=false">
                                <div class="author">
                                    <a href="javascript:void(0)" class="avatar">
                                        <img src="~assets/img/user.jpg">
                                    </a>
                                    <div class="info">
                                        <a class="nickname" href="javascript:void(0)">可可西里里</a>
                                        <a href="javascript:void(0)">
                                            <img class="badge-icon" src="~assets/img/ceshi3.png">
                                        </a>
                                        <span class="time">02.33  15:48</span>
                                    </div>
                                </div>
                                <a class="title" href="javascript:void(0)">
                                    女生都爱的仙女裙怎么穿？
                                </a>
                                <p class="abstract">

                                    文/可可西里里   今天的着装话题说说仙女裙--仙女裙的特点：飘逸柔美，常用的布料是网纱、雪纺、蕾丝等面料.有些美女可能要说仙女裙太薄了，要夏天穿才对--如果这样想那您就奥特...

                                </p>
                                <div class="meta">
                                    <a href="javascript:void(0)">
                                        <i class="fa fa-eye"></i>
                                        4899
                                    </a>
                                    <a href="javascript:void(0)">
                                        <i class="fa fa-comment"></i>
                                        37
                                    </a>
                                    <span>
                                        <i class="fa fa-heart"></i>
                                        45
                                    </span>
                                    <a v-show="showCancel" class="cancel" href="javascript:void(0)">取消关注</a>
                                </div>
                            </div>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    import myHeader from '~/components/myHeader'
    export default {
        data(){
          return{
              showCancel:false
          }
        },
        components:{
            myHeader
        }
    }
</script>
<style>
    .bookmarks .row{
        padding-top: 30px;
    }
    .tag-banner{
        margin-bottom: 30px;
        width: 100%;
        min-height: 100px;
        background-color: rgba(181,181,181,0.098);
        border-radius: 6px;
}
    .note-list li.have-img{
        min-height: 140px;
    }
    .note-list li{
        position: relative;
        width: 100%;
        margin: 0 0 17px;
        padding:0 2px 17px 0;
        border-bottom:1px solid #f0f0f0;
        word-wrap:break-word;
    }
    .note-list .have-img .wrap-img{
        position: absolute;
        top: 50%;
        margin-top:-68px;
        right:0;
        width: 150px;
        height: 120px;
    }
    .note-list .have-img .wrap-img img{
        width: 100%;
        height: 100%;
        border-radius: 4px;
        border:1px solid #f0f0f0;
    }
    .note-list .have-img>div{
        padding-right:160px;
    }
    .note-list .author{
        margin-bottom: 14px;
        font-size: 13px;
    }
    .note-list .author .avatar,.note-list .author .info{
        display: inline-block;
        vertical-align: middle;
    }
    .note-list .author .avatar{
        margin: 0 5px 0 0;
    }
    .note-list .author a{
        color:#333;
    }
    .note-list .author .info .nickname{
        vertical-align: middle;
    }
    .note-list .author .info .badge-icon{
        width: 15px;
        height: 15px;
        margin-left: 3px;
    }
    .note-list .author .info span{
        display: inline-block;
        padding-left: 3px;
        color:#969696;
        vertical-align: middle;
    }
    .note-list .title{
        margin: -7px 0 4px;
        display: inherit;
        font-size: 18px;
        font-weight: 700;
        line-height: 1.5;
    }
    .note-list .abstract{
        margin: 0 0 8px;
        font-size: 13px;
        line-height: 24px;
    }
</style>