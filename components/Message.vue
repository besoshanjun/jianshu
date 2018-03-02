<template>
    <div class="aside">
        <ul>
            <li v-for="(notify,index) in notifys" :key="index" :class="{asideActive:notify.url == path }">
                <nuxt-link :to="notify.url">
                    <i :class="notify.icon"></i>
                    <span>{{notify.title}}</span>
                </nuxt-link>
            </li>
        </ul>
    </div>
</template>
<script>
    export default{
        name:'Message',
        data(){
            return{
                notifys:[
                    {url:'/notify/comments',icon:'fa fa-comment-o',title:'评论'},
                    {url:'/notify/chats',icon:'fa fa-envelope-open-o',title:'简信'},
                    {url:'/notify/requests',icon:'fa fa-upload',title:'投稿请求'},
                    {url:'/notify/likes',icon:'fa fa-heart-o',title:'喜欢和赞'},
                    {url:'/notify/follows',icon:'fa fa-user-o',title:'关注'}
                ],
                path:''
            }
        },
        mounted(){
            this.path = this.$route.path
        }
    }
</script>
<style scoped>
    .aside ul li.asideActive a{
        background-color: #f0f0f0;
        border-radius: 4px;
    }
    .aside ul li:hover{
        background-color: #f0f0f0;
        border-radius: 4px;
    }
    .aside ul li a{
        height: auto;
        padding:10px 25px;
        line-height: 30px;
        display: block;
    }
    .aside ul li i{
        margin-right: 15px;
        font-size: 24px;
        color:#ea6f5a;
        vertical-align: middle;
    }
    .aside ul li span{
        font-size: 15px;
        vertical-align: middle;
    }
</style>