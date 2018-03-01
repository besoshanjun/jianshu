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
                            <div class="content">
                                <div class="author">
                                    <a href="javascript:void(0) class=avatar">
                                        <img src="~assets/img/user.jpg">
                                    </a>
                                    <div class="info">
                                        <a href="javascript:void(0)">可可西里里</a>
                                        <a href="javascript:void(0)">
                                            <img class="" src="~assets/img/ceshi3.png">
                                        </a>
                                    </div>
                                </div>
                                <a class="title" href="javascript:void(0)"></a>
                                <p class="abstract"></p>
                                <div class="meta"></div>
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
</style>