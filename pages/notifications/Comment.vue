<template>
    <div>
        <div class="menu">收到的评论</div>
        <ul class="comment-list" v-for="(notification,index) in notifications">
            <li>
                <nuxt-link to="/u/123" class="avatar">
                    <img src="/user.jpg">
                </nuxt-link>
                <div class="info">
                    <div>
                        <nuxt-link to="/u/123" class="user">
                            {{notification.source.nickname}}
                        </nuxt-link>
                        <span class="comment-slogan">评论了你的文章</span>
                        <nuxt-link to="/p/123">
                           {{notification.target.note.title}}
                        </nuxt-link>
                    </div>
                    <div class="time">{{notification.created_at|formatDate}}</div>
                </div>
                <p>
                   {{notification.target.compiled_content}}
                </p>
                <div class="meta">
                    <a href="javascript:void(0)" class="function-btn">
                        <i class="fa fa-comment-o"></i>
                        <span>回复</span>
                    </a>
                    <nuxt-link to="/p/123" class="function-btn">
                        <i class="fa fa-share"></i>
                        <span>查看对话</span>
                    </nuxt-link>
                </div>
            </li>
        </ul>
        <div v-if="notifications ==''" class="find-nothing">
            <img src="/comment.png">
            <div>这里还没有内容哦~</div>
        </div>
    </div>
</template>
<script>
    export default{
        data(){
            return{
                notifications:[
                    {
                        created_at:"2018-02-05T21:47:58.000+08:00",
                        id: 230409407,
                        is_read: true,
                        source:{
                            avatar_source:'/user.jpg',
                            id: 6099973,
                            nickname:"北纬90度旅行_e3f5",
                            slug:"7120a06c9877",
                        },
                        target:{
                            compiled_content:"我真的来了<br> 带你吃鸡了",
                            id:20345305,
                            note:{
                                id:23143864,
                                slug: "0043e8729f14",
                                title:"测试文章",
                            },
                            parent_id:null,
                            user_id: 6099973,
                        },
                        type: "user_comment_on_note_comment"
                    },
                    {
                        created_at:"2018-02-05T22:47:58.000+08:00",
                        id: 230409408,
                        is_read: true,
                        source:{
                            avatar_source:'/user.jpg',
                            id: 6099974,
                            nickname:"hahaha",
                            slug:"7120a06c9877",
                        },
                        target:{
                            compiled_content:"厉害了",
                            id:20345305,
                            note:{
                                id:23143864,
                                slug: "0043e8729f14",
                                title:"测试文章",
                            },
                            parent_id:null,
                            user_id: 6099973,
                        },
                        type: "user_comment_on_note_comment"
                    }
                ]
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
    .notification .main .comment-list .avatar{
        display: inline-block;
        margin-right: 5px;
        width: 40px;
        height: 40px;
    }
    .notification .main .comment-list .info{
        display:inline-block;
        vertical-align: top;
        width: 535px;
        font-size: 15px;
        line-height: 1.7;
    }
    .notification .main .comment-list .info .user{
        margin: 0 5px 0 0;
        color:#333;
    }
    .notification .main .comment-list .info .comment-slogan{
        font-size: 15px;
        color:#333;
    }
    .notification .main .comment-list .info a{
        font-size: 15px;
        color:#3194d0 !important;
    }
    .notification .main .comment-list .info .time{
        margin-top: 2px;
        font-size: 12px;
        color: #969696;
        line-height: normal;
    }
    .notification .main .comment-list .info p{
        margin:10px 0 0;
        font-size: 15px;
        line-height: 1.7;
    }
    .notification .main .comment-list .meta{
        margin-top: 10px;
        height: 20px;
    }
    .notification .main .comment-list .meta .function-btn{
        float: left;
        margin-right: 30px;
        font-size: 13px;
        color:#969696 !important;
    }
    .notification .main .comment-list .meta .function-btn:hover{
        color:#333!important;
    }
    .notification .main .comment-list .meta .function-btn i{
        margin-right: 5px;
        font-size: 15px;
        vertical-align: middle;
    }
    .notification .main .comment-list .meta .function-btn span{
        vertical-align: middle;
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