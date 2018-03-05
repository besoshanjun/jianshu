<template>
    <div class="list-container">
        <ul class="user-list">
            <li>
                <a class="avatar" href="javascript:void(0)">
                    <img src="~assets/img/user.jpg">
                </a>
                <div class="info">
                    <a class="name" href="javascript:void(0)">疯自在_945</a>
                    <div class="meta">
                        <span> 关注 123</span>
                        <span>粉丝 298</span>
                        <span>文章 80</span>
                    </div>
                    <div class="meta">
                        写了60310字，获得2761个喜欢
                    </div>
                </div>
                <a href="javascript:void(0)" class="follow">
                    <i class="fa" :class="iconObj" ref="icon"></i>
                    <span ref="followWord">关注</span>
                </a>
            </li>
        </ul>
    </div>
</template>
<script>
    export default{
        name:'Followers',
        data(){
            return{
                followObj: {
                    'follow': true,
                    'following': false
                },
                iconObj: {
                    'fa-plus-square-o': true,
                    'fa-check': false
                },
            }
        },
        methods:{
            isFollow: function () {
                let word = this.$refs.followWord.innerHTML;
                this.followObj.follow = !this.followObj.follow;
                this.followObj.following = !this.followObj.following;
                this.iconObj['fa-plus-square-o'] = !this.iconObj['fa-plus-square-o'];
                this.iconObj['fa-check'] = !this.iconObj['fa-check'];
                this.$refs.followWord.innerHTML = word == '关注' ? '已关注' : '关注';
            },
            noFollow: function () {
                let word = this.$refs.followWord.innerHTML;
                if (word == '已关注') {
                    this.$refs.followWord.innerHTML = '取消关注';
                    this.$refs.icon.className = 'fa fa-close';
                }
            },
            beFollow: function () {
                let word = this.$refs.followWord.innerHTML;
                if (word == '取消关注') {
                    this.$refs.followWord.innerHTML = '已关注';
                    this.$refs.icon.className = 'fa fa-check';
                }
            },
        }
    }
</script>
<style>
    .list-container .user-list li:first-child{
        padding-top: 0!important;
    }
    .list-container .user-list li{
        padding-bottom: 20px;
        margin-bottom: 20px;
        border-bottom: 1px solid #f0f0f0;
        line-height: normal;
    }
    .list-container .user-list .info{
        vertical-align: middle;
        display: inline-block;
        max-width: 450px;
    }
    .list-container .user-list .info a{
        font-size: 15px;
        font-weight: 700;
        color: #333;
    }
    .list-container .user-list .meta{
        padding-top: 2px;
        font-size: 12px;
        color:#969696;
    }
    .list-container .user-list .meta span{
        margin-right: 10px;
        padding-right: 10px;
        border-right: 1px solid #969696;
    }
</style>