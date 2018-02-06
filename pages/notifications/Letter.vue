<template>
    <div>
        <div class="menu">全部简信</div>
        <ul class="jianxin-list">
            <li  v-for="(chat,index) in chats" @click="unread_message(index)">
                <nuxt-link to="/u/123" class="avatar">
                    <img src="/user.jpg">
                    <span class="badge">{{chat.unread_messages_count}}</span>
                </nuxt-link>
                <div class="pull-right">
                    <span class="time">2018.1.25</span>
                    <div class="open">
                        <a href="javascript:void(0)" @click="dropdown(index)">
                            <i class="arrowdown"></i>
                        </a>
                        <ul v-if="true" class="dropmenu">
                            <li>
                                <a href="javascript:void(0)" @click="removeBack(index)">
                                    <i class="fa fa-times"></i>
                                    删除回话
                                </a>
                            </li>
                            <li>
                                <a href="javascript:void(0)">
                                    <i class="fa fa-times"></i>
                                    加入黑名单
                                </a>
                            </li>
                            <li>
                                <a href="javascript:void(0)">
                                    <i class="fa fa-times"></i>
                                    举报用户
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>
                <nuxt-link to="/u/123" class="name">
                    {{chat.user.nickname}}
                </nuxt-link>
                <nuxt-link to="/message" class="wrap">
                    <p>{{chat.last_message_content}}</p>
                </nuxt-link>
            </li>
        </ul>
        <div v-if="chats ==''" class="find-nothing">
            <img src="/comment.png">
            <div>这里还没有内容哦~</div>
        </div>
    </div>
</template>
<script>
    export default{
        data(){
            return{
                chats:[
                    {
                       id:481237859,
                        last_message_content: " 欢迎加入丰富多彩的原创内容社区—简书。新手有关简书的任何疑问请点击链接查看 http://w...",
                        last_message_created_at: 1516932408281,
                        unread_messages_count: 1,
                        user:{
                            avatar_source:'/user.jpg',
                            id: 3678149,
                            is_blocking_user: false,
                            nickname: "简宝玉",
                            slug: "b52ff888fd17"
                        }

                    },
//                    {
//                        id:481237850,
//                        last_message_content: " 12345677654321,狂拽酷帅屌炸天，我们javascript语言最牛逼，茫茫人海中遇见你。",
//                        last_message_created_at: 1516932408280,
//                        unread_messages_count: 4,
//                        user:{
//                            avatar_source:'/user.jpg',
//                            id: 3678148,
//                            is_blocking_user: false,
//                            nickname: "大哥哥",
//                            slug: "b52ff888fd17"
//                        }
//
//                    }
                ]
            }
        },
        methods:{
            unread_message(index){
                this.chats[index].unread_messages_count = ''
            }
        }
    }
</script>
<style>
    .notification .main .menu{
        margin-bottom: 20px;
        font-size: 14px;
        font-weight: 700;
    }
    .notification .main .jianxin-list>li{
        position: relative;
        border-top:1px solid #f0f0f0;
    }
    .notification .main .jianxin-list .avatar{
        float:left;
        margin: 20px 10px 20px 20px;
        width: 48px;
        height: 48px;
    }
    .notification .main .jianxin-list .name{
        position: absolute;
        top:25px;
        font-size: 15px;
    }
    .notification .main .jianxin-list .avatar .badge{
        position: relative;
        float:right;
        top:-48px;
        right:-5px;
    }
    .notification .main .jianxin-list .pull-right{
        float:right;
        margin: 20px 40px 0 0;
        font-size: 13px;
    }
    .notification .main .jianxin-list .pull-right .open>a{
        position: absolute;
        right:30px;
        top:28px;
    }
    .notification .main .jianxin-list .pull-right .open .arrowdown:after{
        width: 8px;
        height: 8px;
        content: "";
        position: absolute;
        border-left: 1px solid #aaa;
        border-top: 1px solid #aaa;
        transform: translate3d(0,-50%,0) rotate(-135deg);
        -webkit-transform: translate3d(0,-50%,0) rotate(-135deg);
    }
    .notification .main .jianxin-list .pull-right .open .dropmenu{
        position: absolute;
        background: #fff;
        padding: 5px 0;
        min-width: 136px;
        top:45px;
        right: 15px;
        border: 1px solid #f0f0f0;
        box-shadow: 0 0 10px #999;
    }
    .notification .main .jianxin-list .pull-right .open .dropmenu li:hover{
        background: #f0f0f0;
    }
    .notification .main .jianxin-list .pull-right .open .dropmenu li a{
        font-size: 14px;
        display: block;
        padding: 10px 20px;
        font-weight: 400;
        color:#333 !important;
    }

    .notification .main .jianxin-list .pull-right .open .dropmenu li a i{
        margin-right: 10px;
        font-size: inherit;
    }
    .notification .main .jianxin-list .wrap{
        display: block;
        padding: 20px 20px 20px 0;
        min-height: 88px;
    }
    .notification .main .jianxin-list .wrap p{
        margin:28px 0 0;
        font-size: 12px;
        color:#999;
        overflow: hidden;
        text-wrap: ellipsis;
        white-space: nowrap;
    }
    .notification .main .find-nothing{
        margin-top: 150px;
        text-align: center;
    }
    .notification .main .find-nothing img{
        width: 100px;
    }
    .notification .main .find-nothing div{
        margin-top: 20px;
        font-size: 14px;
        font-weight: 700;
    }
</style>