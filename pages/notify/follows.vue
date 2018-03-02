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
                        <div class="menu">全部关注</div>
                        <ul class="follow-list">
                            <li>
                                <a href="/u/123" class="avatar">
                                    <img src="~assets/img/user.jpg">
                                </a>
                                <div class="info">
                                    <a href="/u/123" class="user">北纬90度旅行_e3f5</a>
                                    <span>关注了你</span>
                                    <div class="time">2018.03.01 17:29</div>
                                </div>
                                <a href="javascript:void(0)" class="btn btn-default following">
                                    <i class="fa fa-check"></i>
                                    <span>已关注</span>
                                </a>
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