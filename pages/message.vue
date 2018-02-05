<template>
    <div class="notification">
        <my-header></my-header>
        <div class="my-container">
            <div class="row">
                <div class="aside col-4">
                    <ul>
                        <li :class="{active:isComment}">
                            <a href="javascript:void(0)" @click="active('Comment')">
                                <i class="fa fa-comment-o"></i>
                                <span>评论</span>
                            </a>
                        </li>
                        <li :class="{active:isLetter}">
                            <a href="javascript:void(0)" @click="active('Letter')">
                                <i class="fa fa-envelope-open-o"></i>
                                <span>简信</span>
                            </a>
                        </li>
                        <li :class="{active:isContribute}">
                            <a href="javascript:void(0)" @click="active('Contribute')">
                                <i class="fa fa-upload"></i>
                                <span>投稿请求</span>
                            </a>
                        </li>
                        <li :class="{active:isLike}">
                            <a href="javascript:void(0)" @click="active('Like')">
                                <i class="fa fa-heart-o"></i>
                                <span>喜欢和赞</span>
                            </a>
                        </li>
                        <li :class="{active:isAttention}">
                            <a href="javascript:void(0)" @click="active('Attention')">
                                <i class="fa fa-user-o"></i>
                                <span>关注</span>
                            </a>
                        </li>
                    </ul>
                </div>
                <div class="col-8 main">
                    <component :is="names"></component>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    import myHeader from '~/components/myHeader'
    import Comment from '~/pages/notifications/Comment'
    import Letter from '~/pages/notifications/Letter'
    import Contribute from '~/pages/notifications/Contribute'
    import Like from '~/pages/notifications/Like'
    import Attention from '~/pages/notifications/Attention'
    export default{

        data(){
            return {
                names: 'Comment',
                isComment: false,
                isContribute: false,
                isLetter: false,
                isLike: false,
                isAttention: false
            }
        },
        methods: {
            active(value){
                this.names = value;
                this.isComment = false;
                this.isContribute = false;
                this.isLetter = false;
                this.isLike = false;
                this.isAttention = false
                switch (value) {
                    case 'Comment':
                        this.isComment = true;
                        break;
                    case 'Contribute':
                        this.isContribute = true;
                        break;
                    case 'Letter':
                        this.isLetter = true;
                        break;
                    case 'Like':
                        this.isLike = true;
                        break;
                    case 'Attention':
                        this.isAttention = true;
                        break;
                }
            }
        },
        components: {
            myHeader,
            Comment,
            Contribute,
            Letter,
            Like,
            Attention
        }
    }
</script>
<style>
    .notification .row {
        padding: 30px 0;
    }

    .notification .aside ul li {
        margin: 0;
        line-height: 20px;
    }

    .notification .aside ul li a {
        height: auto;
        padding: 10px 25px;
        line-height: 30px;
        display: block;
    }

    .notification .aside ul li.active a {
        background: #f0f0f0;
        border-radius: 4px;
    }

    .notification .aside ul li a:hover {
        background: #f0f0f0;
        border-radius: 4px;
    }

    .notification .aside ul li a i {
        font-size: 24px;
        color: #ea6f5a;
        margin-right: 15px;
        vertical-align: middle;
    }

    .notification .aside ul li a span {
        font-size: 15px;
        vertical-align: middle;
    }
</style>