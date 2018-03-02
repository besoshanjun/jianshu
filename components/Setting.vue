<template>
    <div>
        <div class="my-container">
            <div class="col-4">
                <ul>
                    <li class="basic">
                        <nuxt-link to="/settings/basic">
                            <div class="setting-icon">
                                <i class="fa fa-list-ul"></i>
                            </div>
                            <span>基础设置</span>
                        </nuxt-link>
                    </li>
                    <li class="profile">
                        <nuxt-link to="/settings/profile">
                            <div class="setting-icon">
                                <i class="fa fa-address-book-o"></i>
                            </div>
                            <span>个人资料</span>
                        </nuxt-link>
                    </li>
                    <li class="misc">
                        <nuxt-link to="/settings/misc">
                            <div class="setting-icon">
                                <i class="fa fa-cog"></i>
                            </div>
                            <span>账号管理</span>
                        </nuxt-link>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>
<script>
    export default{
        name:'Setting'
    }
</script>
<style scoped>
    li{
        line-height: 20px;
    }
    li:hover{
        background-color: #f0f0f0;
        border-radius: 4px;
    }
    a{
        padding: 10px 15px;
        font-size: 15px;
        display:block;
    }
    .setting-icon{
        margin-right: 15px;
        width: 32px;
        height: 32px;
        text-align: center;
        color: #fff;
        background-color: #a0a0a0;
        border-radius: 4px;
        display: inline-block;
        vertical-align: middle;
    }
    .setting-icon i{
        margin: 8px 0 0 1px;
        font-size: 18px;
        display: block;
    }
    span{
        vertical-align: middle;
    }
</style>