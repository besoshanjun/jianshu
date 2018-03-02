<template>
    <div>
        <nav class="navbar navbar-default nav-fixed-top">
            <div class="width-limit">
                <!--logo-->
                <nuxt-link class="nav-logo" to="/">
                    <img src="../assets/img/nav-logo.png">
                </nuxt-link>
                <nuxt-link class="btn write-btn" to="/create">
                    <i class="fa fa-pied-piper"></i>
                    写文章
                </nuxt-link>
                <!--登录和注册按钮-->
                <!--<nuxt-link to="/sign-up" class="btn sign-up">注册</nuxt-link>-->
                <!--<nuxt-link to="/sign-in" class="btn sign-in">登录</nuxt-link>-->
                <!--如果用户登录，那么显示用户头像-->
                <div class="user" @mouseover="userShow=true" @mouseout="userShow=false">
                    <div class="drop-down">
                        <nuxt-link class="avatar" to="/u/123">
                            <img src="../assets/img/user.jpg">
                        </nuxt-link>
                    </div>
                    <div class="drop-menu" v-show="userShow">
                        <ul>
                            <li>
                                <nuxt-link to="/u/123">
                                    <i class="fa fa-user"></i>
                                    我的主页
                                </nuxt-link>
                            </li>
                            <li>
                                <nuxt-link to="/bookmarks">
                                    <i class="fa fa-bookmark"></i>
                                    收藏的文章
                                </nuxt-link>
                            </li>
                            <li>
                                <nuxt-link to="/users/123/like">
                                    <i class="fa fa-heart"></i>
                                    喜欢的文章
                                </nuxt-link>
                            </li>
                            <li>
                                <nuxt-link to="/settings/basic">
                                    <i class="fa fa-cog"></i>
                                    设置
                                </nuxt-link>
                            </li>
                            <li>
                                <nuxt-link to="/logout">
                                    <i class="fa fa-sign-out"></i>
                                    退出
                                </nuxt-link>
                            </li>
                        </ul>
                    </div>
                </div>
                <!--导航-->
                <div class="my-container">
                    <ul class="nav-list">
                        <li class="active">
                            <nuxt-link to="/">
                                <i class="fa fa-compass"></i>
                                <span>发现</span>
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/">
                                <i class="fa fa-book"></i>
                                <span>关注</span>
                            </nuxt-link>
                        </li>
                        <li class="notify" @mouseover="notifyShow=true" @mouseleave="notifyShow=false">
                            <nuxt-link to="/notify/comments">
                                <i class="fa fa-bell-o"></i>
                                <span>消息</span>
                            </nuxt-link>
                            <div class="drop-menu" v-if="notifyShow">
                                <ul>
                                    <li>
                                        <nuxt-link to="/notify/comments">
                                            <i class="fa fa-comment-o"></i>
                                            评论
                                        </nuxt-link>
                                    </li>
                                    <li>
                                        <nuxt-link to="/notify/chats">
                                            <i class="fa fa-envelope-open-o"></i>
                                            简信
                                        </nuxt-link>
                                    </li>
                                    <li>
                                        <nuxt-link to="/notify/requests">
                                            <i class="fa fa-upload"></i>
                                            投稿请求
                                        </nuxt-link>
                                    </li>
                                    <li>
                                        <nuxt-link to="/notify/likes">
                                            <i class="fa fa-heart-o"></i>
                                            喜欢和赞
                                        </nuxt-link>
                                    </li>
                                    <li>
                                        <nuxt-link to="/notify/follows">
                                            <i class="fa fa-user-o"></i>
                                            关注
                                        </nuxt-link>
                                    </li>
                                </ul>
                            </div>
                        </li>
                        <li class="search">
                            <form method="post">
                                <input class="input" ref="input" placeholder="搜索" type="text" @focus="bgShow=true" @blur="bgShow=false">
                                <nuxt-link class="search-btn" :class="{active:bgShow}" to="/search"><i class="fa fa-search"></i></nuxt-link>
                            </form>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>
    </div>
</template>
<script>
    export default{
        data(){
            return {
                userShow: false,
                notifyShow:false,
                bgShow:false,
            }
        },
        name: 'myHeader',
    }
</script>
<!--scoped 只在当前组件中使用以下css样式-->
<style scoped>
    ul,ol,dl{
        margin: 0;
    }
    nav {
        width: 100%;
        height: 56px;
    }
    .navbar {
        padding: 0;
        border-bottom: 1px solid #e7e7e7;
        margin-bottom: 20px;
        background-color: #fff;
    }
    .nav-fixed-top {
        position: fixed;
        top: 0;
        left: 0;
        z-index: 9999;
    }
    nav .width-limit {
        min-width: 768px;
        width: 1440px;
        margin: 0 auto;
    }
    nav .nav-logo {
        float: left;
        height: 56px;
        padding: 0;
    }
    nav a.write-btn {
        float: right;
        margin: 9px 0 0 0;
        line-height: 24px;
        font-size: 16px;
        background-color: #ea6f5a;
        color: #fff !important;
        border-radius: 20px;
        margin: 8px 15px 0;
    }
    nav a.write-btn:hover {
        background: #ec6149;
    }
    nav a.sign-in{
        float: right;
        height: 35px;
        margin: 10px 6px 0 10px;
        padding: 6px 12px;
        line-height: 24px;
        font-size: 15px;
        color: #969696 !important;
        box-shadow: none;
    }
    nav a.sign-up{
        float: right;
        width: 80px;
        height: 38px;
        margin: 10px 16px 0 10px;
        padding: 6px 12px;
        line-height: 24px;
        font-size: 15px;
        border:1px solid #ea6f5a;
        border-radius: 20px;
        color:#ea6f5a !important;
        box-shadow: none;
    }
    nav a.sign-up:hover{
        background-color: rgb(254,247,246);
    }
    nav .user {
        float: right;
        position: relative;
    }
    nav .user .avatar {
        width: 40px;
        height: 40px;
        display: block;
        position: relative;
        margin: 8px 28px 8px 20px;
    }
    nav .user .avatar img {
        width: 100%;
        height: 100%;
        border: 1px solid #ccc;
        border-radius: 50%;
    }
    nav .user .avatar:before {
        content: "";
        position: absolute;
        top: 18px;
        right: -14px;
        border-left: 5px solid transparent;
        border-right: 5px solid transparent;
        border-top: 6px solid #999;
    }
    nav .user:hover {
        background: #f5f5f5;
    }
    nav .user .drop-menu {
        position: absolute;
        left: 0;
        z-index: 999;
        min-width: 160px;
        box-shadow: 0 0 8px rgba(0, 0, 0, .1);
        font-size: 15px;
        background: #fff;
    }
    nav .user .drop-menu ul {
        border: 1px solid #ccc;
        padding: 10px 0;
        margin: 0;
    }
    nav .user .drop-menu ul li a {
        padding: 10px 20px;
        display: block;
    }
    nav .user .drop-menu ul li a:hover {
        background: #f5f5f5;
    }
    nav .user .drop-menu ul li i {
        margin-right: 15px;
        color: #ea6f5a;
        font-size: 18px;
    }
    nav .nav-list{
        margin:  0 -15px;
        padding: 0;
    }
    nav .nav-list:after{
        content: "";
        height: 0;
        visibility: hidden;
        display: block;
        clear: both;
    }
    nav .nav-list>li {
        float: left;
        margin-right: 5px;
    }
    nav .nav-list>li:hover{
        background-color:#f5f5f5;
    }
    nav .nav-list>li>a {
        display: block;
        height: 55px;
        padding: 15px;
        margin-right: 10px;
        font-size: 17px;
    }
    nav .nav-list>li>a>i {
        margin-right: 7px;
        margin-top: 5px;
        font-size: 20px;
    }
    nav .nav-list>li.active {
        color: #ea6f5a;
        background-color: #fff;
    }
    nav .nav-list  .notify{
        position: relative;
    }
    nav .notify .drop-menu {
        position: absolute;
        left: 0;
        z-index: 999;
        min-width: 160px;
        box-shadow: 0 0 8px rgba(0, 0, 0, .1);
        font-size: 15px;
        background: #fff;
    }
    nav .notify .drop-menu ul {
        border: 1px solid #ccc;
        padding: 10px 0;
        margin: 0;
    }
    nav .notify .drop-menu ul li a {
        padding: 10px 20px;
        display: block;
    }
    nav .notify .drop-menu ul li a:hover {
        background: #f5f5f5;
    }
    nav .notify .drop-menu ul li i {
        margin-right: 15px;
        color: #ea6f5a;
        font-size: 18px;
    }
    nav .nav-list .search:hover{
        background: #fff;
    }
    nav .nav-list .search{
        padding-left: 15px;
    }
    nav .nav-list .search form{
        margin-top: 9px;
        position: relative;
    }
    nav .nav-list .search form input{
        width: 240px;
        height: 38px;
        border: none;
        background: rgb(238,238,238);
        border-radius: 20px;
        padding:0 40px 0 20px;
        font-size: 15px;
        transition: width ease-in .3s ;
    }
    nav .nav-list .search form input:focus{
        width:320px;
    }
    nav .nav-list .search form a.search-btn{
        width: 30px;
        height: 30px;
        position: absolute;
        right:5px;
        top: 4px;
        text-align: center;
        line-height: 30px;
        color: #969696 !important;
    }
    nav .nav-list .search form a.active{
        background: #969696;
        border-radius: 50%;
        color: #fff !important;
        font-size: 18px;
        color: #969696;
    }
    @media(max-width:768px){
        nav .nav-list{
            display: none;
        }
    }
    @media (max-width: 1440px) {
        nav .nav-list>li>a>i {
            display: none;
        }
        nav .nav-list .search form input{
            width:160px;
        }
        nav .nav-list .search form input:focus{
            width:240px;
        }
    }

    @media (max-width: 1080px) {
        nav .nav-list>li>a>i {
            display: block;
        }

        nav .nav-list>li>a>span {
            display: none;
        }
        nav .nav-list .search form input{
            width:150px;
        }
        nav .nav-list .search form input:focus{
            width:150px;
        }
    }
</style>