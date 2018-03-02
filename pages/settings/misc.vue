<template>
  <div>
   <my-header></my-header>
   <div class="setting my-container">
       <div class="row">
           <div id="aside" class="col-4">
               <setting></setting>
           </div>
           <div class="main col-8">
              <table>
                  <tbody>
                   <tr>
                       <td class="setting-title">打包下载文章</td>
                       <td>
                          <a href="javascript:void(0)" class="btn-hollow">下载所有文章</a>
                       </td>
                   </tr>
                  </tbody>
              </table>
              <div class="delete-account-content">
                  <a href="javascript:void(0)" class="show-button" v-if="show" @click="is_show">
                      删除账号
                      <i class="fa fa-angle-down"></i>
                  </a>
                  <div class="content" v-if="content">
                      <h4>永久删除账号</h4>
                      <ul>
                          <li>
                              如果你不小心创建出了多余的帐号，或在绑定帐号的时候提示帐号被占用，你可以在<nuxt-link to="/p/123">简书帐号绑定解绑相关问题汇总</nuxt-link>中获得相关帮助。
                          </li>
                          <li>
                              如果你对简书上的某些内容、功能或社区规则不满意，你可以在<a href="javascript:void(0)">帮助与反馈页</a>向我们提出。
                          </li>
                          <li>删除帐号前，请确保已经没有任何公开或私密文章，且钱包中全部余额已清零。</li>
                          <li>删除帐号是不可逆的操作，删除后将无法恢复。</li>
                      </ul>
                      <a href="javascript:void(0)" class="btn-hollow" @click="is_content">保留我的账号</a>
                      <a href="javascript:void(0)" class="btn-delete">删除账号</a>
                  </div>
              </div>
           </div>
       </div>
   </div>
  </div>
</template>
<script>
import MyHeader from "~/components/myHeader";
import Setting from '~/components/Setting'
export default {
  name:'basic',
  data(){
      return{
          content:false,
          show:true,
      }
  },
    mounted(){
        let value = document.querySelector('#aside ul .misc')
        value.className = 'asideActive'
    },
  methods:{
      is_show(){
        this.content=true;
        this.show=false;
      },
      is_content(){
          this.content=false;
          this.show=true;
      }
  },
  components:{
      MyHeader,
      Setting
  }
}
</script>
<style scoped>
    .row{
        padding-top: 30px;
    }
table{
    width: 100%;
}
.setting .main .setting-title{
    font-size: 15px;
    color: #969696;
}
.setting .main .btn-hollow{
    font-size: 14px;
    border: 1px solid ;
    color:#42c02e!important;
    padding: 4px 12px;
    border-radius: 40px;
    display: inline-block;
}
.setting .main tr{
    border-bottom: 1px solid #f0f0f0;
}
.setting .main tr td{
    padding-bottom: 20px;
}
.setting .main .delete-account-content{
    padding-top: 20px;
    font-size: 15px;
}
.setting .main .delete-account-content>a{
    color: #969696!important;
}
.setting .main .delete-account-content .content li{
    list-style:disc;
    padding:5px 0 5px;
    font-size: 14px;
}
.setting .main .delete-account-content .content ul li a{
    color: #3194d0!important;
}
.setting .main .delete-account-content .content .btn-hollow{
    margin-top: 10px;
    margin-right: 10px;
}
.setting .main .btn-delete{
    font-size: 14px;
    border: 1px solid ;
    color:#ea6f5a!important;
    padding: 4px 12px;
    display: inline-block;
    border-radius: 40px;
}
</style>
