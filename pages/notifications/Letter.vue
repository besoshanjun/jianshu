<template>
    <div>
        <div class="menu">全部简信</div>
        <ul class="jianxin-list" v-for="(notification,index) in notifications">
            <li>
                <nuxt-link to="/u/123" class="avatar">
                    <img src="/user.jpg">
                    <span class="badge">1</span>
                </nuxt-link>
                <div class="pull-right">
                    <span class="time">1321654</span>
                    <div></div>
                </div>
                <nuxt-link to="/u/123" class="name">
                    简宝玉
                </nuxt-link>
                <nuxt-link to="/">
                    <p> 欢迎加入丰富多彩的原创内容社区—简书。新手有关简书的任何疑问请点击链接查看 http://w...</p>
                </nuxt-link>
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
    .notification .main .jianxin-list .avatar{
        display: inline-block;
        margin-right: 5px;
        width: 40px;
        height: 40px;
    }
    .notification .main .jianxin-list .avatar .badge{
        position: relative;
        float:right;
        top:-48px;
        right:-5px;
    }
    .notification .main .jianxin-list .pull-right{
        float:right;
        margin: 20px 20px 0 0;
        font-size: 13px;
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