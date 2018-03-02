<template>
    <div class="notify">
        <my-header></my-header>
        <div class="my-container">
            <div class="row">
                <div class="col-4" style="width: 280px">
                    <message></message>
                </div>
                <div class="col-8 main">
                    <div>
                        <div class="menu">收到的评论</div>
                        <ul class="comment-list">
                            <li>
                                <a class="avatar" href="/u/123">
                                    <img src="~assets/img/user.jpg">
                                </a>
                                <div class="info">
                                    <div>
                                        <a href="/u/123" class="user">北纬90度旅行_a3f5</a>
                                        <span class="comment-slogan">评论了你的文章</span>
                                        <a href="/p/123">《测试文章》</a>
                                    </div>
                                    <div class="time">2018.02.05 21:47</div>
                                </div>
                                <p>
                                    我真的来了<br>带你吃鸡了
                                </p>
                                <div class="meta">
                                    <a href="javascript:void(0)" class="function-btn">
                                        <i class="fa fa-comment-o"></i>
                                        <span>回复</span>
                                    </a>
                                    <a href="javascript:void(0)" class="function-btn">
                                        <i class="fa fa-share"></i>
                                        <span>查看对话</span>
                                    </a>
                                </div>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    import myHeader from'~/components/myHeader'
    import Message from '~/components/Message'
    export default{
        components: {
            myHeader,
            Message
        }
    }
</script>
<style>

</style>