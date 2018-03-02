<template>
    <div class="notify">
        <my-header></my-header>
        <div class="my-container">
            <div class="row">
                <div class="col-4">
                    <message></message>
                </div>
                <div class="col-8 main">
                    <div>
                        <div class="menu">收到的喜欢和赞</div>
                        <ul class="like-list">
                            <li>
                                <a href="/u/123" class="avatar">
                                    <img src="~assets/img/user.jpg">
                                </a>
                                <div class="info">
                                    <a href="/u/123" class="user">大哥哥4555</a>
                                    <span>赞你的评论</span>
                                    <a href="/p/123" class="middle">厉害了</a>
                                    <div class="time">
                                        2018.2.06 09:24
                                    </div>
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