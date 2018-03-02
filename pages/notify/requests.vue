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
                        <div class="menu">全部投稿请求</div>
                        <ul class="push-list">
                            <li>
                                <a href="javascript:void(0)" class="wrap">
                                    <div class="all-push">
                                        <i class="fa fa-upload"></i>
                                    </div>
                                    <div class="name">全部未处理请求</div>
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