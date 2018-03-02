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
                        <div class="menu">全部简信</div>
                        <ul class="jianxin-list">
                            <li>
                                <div class="pull-right">
                                    <span class="time">02.06 09:24</span>
                                    <div class="open">
                                        <a href="javascript:void(0)" @click="showDropDownMenu()" style="margin-left: 3px;font-size: 18px;">
                                            <i class="fa fa-angle-down"></i>
                                        </a>
                                        <ul class="dropdown-menu" v-show="showMenud">
                                            <li>
                                                <a href="javascript:void(0)">
                                                <i class="fa fa-trash-o"></i>
                                                    删除回话
                                            </a>
                                            </li>
                                            <li>
                                                <a href="javascript:void(0)">
                                                    <i class="fa fa-ban"></i>
                                                   加入黑名单
                                                </a>
                                            </li>
                                            <li>
                                                <a href="javascript:void(0)">
                                                    <i class="fa fa-flag-o"></i>
                                                    举报用户
                                                </a>
                                            </li>
                                        </ul>
                                    </div>
                                </div>
                                <a href="/u/123" class="avatar">
                                    <img src="~assets/img/user.jpg">
                                </a>
                                <a href="/u/123" class="name">大哥哥4555</a>
                                <a href="javascript:void(0)" class="wrap">
                                    <p>茫茫人海遇见你，缘分</p>
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
        data(){
          return{
              showMenud:false
          }
        },
        methods:{
            showDropDownMenu(){
                console.log(this.showMenud)
                this.showMenud = !this.showMenud
            }
        },
        components: {
            myHeader,
            Message
        }
    }
</script>
<style>

</style>