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
                           <td class="setting-title pull-left">性别</td>
                           <td class="sex">
                                <input type="radio" name="sex" id="">
                               <span>男</span>
                               <input type="radio" name="sex" id="">
                               <span>女</span>
                               <input type="radio" name="sex" id="" checked>
                               <span>保密</span>
                           </td>
                       </tr>
                       <tr>
                           <td class="setting-title">个人简介</td>
                           <td class="line">
                               <form>
                                   <textarea placeholder="请填写你的个人简介"></textarea>
                               </form>
                           </td>
                       </tr>
                       <tr>
                           <td class="setting-title">个人网站</td>
                           <td class="line">
                               <form>
                                   <input type="text" placeholder="https://你的网址">
                                    <p class="pull-right">填写后会在个人主页显示图标</p>
                               </form>
                           </td>
                       </tr>
                       <tr>
                           <td class="setting-title">微信二维码</td>
                           <td class="weixin-qrcode line">
                               <input type="file" class="hide">
                               <a href="javascript:void(0)" class="btn-hollow">
                                   更换照片
                               </a>
                               <p class="pull-right">上传后会在个人主页显示图标</p>
                           </td>
                       </tr>
                       <tr>
                           <td class="setting-title">社交账号</td>
                           <td class="social-bind line">
                               <p>你可以通过绑定的社交帐号登录简书。出于安全因素, 你最初用来创建账户的社交帐号不能移除。</p>
                               <p>如果帐号被占用，你可以在<a href="javascript:void(0)">简书帐号绑定解绑相关问题汇总</a>中获得相关帮助。</p>
                                <ul class="social-list">
                                    <li><i class="fa fa-weibo"></i><a href="javascript:void(0)">绑定微博<i class="fa fa-angle-right"></i></a></li>
                                    <li><i class="fa fa-weixin"></i><a href="javascript:void(0)">绑定微信<i class="fa fa-angle-right"></i></a></li>
                                    <li><i class="fa fa-qq"></i><a href="javascript:void(0)">绑定QQ<i class="fa fa-angle-right"></i></a></li>
                                    <li><i class="fa fa-bug"></i><a href="javascript:void(0)">绑定豆瓣<i class="fa fa-angle-right"></i></a></li>
                                    <li><i class="fa fa-google-plus"></i><a href="javascript:void(0)">绑定 Google+<i class="fa fa-angle-right"></i></a></li>
                                </ul>
                           </td>
                       </tr>
                   </tbody>
               </table>
                <button type="submit" class="save">保存</button>
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
  components:{
      MyHeader,
      Setting
  },
    mounted(){
        let value = document.querySelector('#aside ul .profile')
        value.className = 'asideActive'
    },
}
</script>
<style scoped>
    .row{
        padding-top: 30px;
    }
table{
    width: 625px;
}
.setting .main tr{
    border-bottom: 1px solid #f0f0f0;
}
.setting .main tr:last-child{
    border: none;
}
.setting .main tr td{
    padding: 20px 0 20px;
}
.setting .main .setting-title{
    font-size: 15px;
    color: #969696;
}
.setting .main tr td:first-child{
    width: 100px;
}
.setting .main input[type="radio"]{
  margin-right: 10px;
}

.setting .main .sex span{
    margin-right: 20px;
}
.setting .main tr td:nth-of-type(2){
    padding-left: 20px;
}
.setting .main textarea{
    width: 100%;
    height: 100px;
    margin-bottom: 10px;
    padding: 8px 10px;
    font-size: 15px;
    border: 1px solid #c8c8c8;
    border-radius: 4px;
    resize: none;
    outline-style: none;
    background-color:#F7F7F7;
}
.setting .main input[type="text"]{
    width: 100%;
    padding: 5px 10px;
    font-size: 15px;
    border: 1px solid #c8c8c8;
    border-radius: 4px;
    margin-bottom: 10px;
    background-color: #f7f7f7;
}
.setting .main p{
    padding-top: 8px;
    font-size: 12px;
    color: #969696;
    margin: 0;

}
.setting .main .hide{
   position: absolute;
  opacity: 0;
  width: 82px;
}
.setting .main .btn-hollow{
    font-size: 14px;
    padding: 4px 12px;
    border-radius: 40px;
    border:1px solid #42c02e;
    color: #42c02e!important;
}
.setting .main p a{
    color: #3194d0!important;
}
.setting .main .social-list li{
    border-bottom: 1px solid #f0f0f0;
    line-height: 50px;
}
.setting .main .social-list li:last-child{
    border: 0;
}
.setting .main .social-list i{
    margin-right: 20px;
    font-size: 20px;
    display: inline-block;
    vertical-align: middle;
}
.setting .main .social-list a{
    font-size: 14px;
    vertical-align: middle;
}
.setting .main .social-list a i{
    font-size: 14px;
    margin-left: 5px;
}
.setting .main .social-list .fa-weibo{
    color: #ea6f5a;
}
.setting .main .social-list .fa-weixin{
    color:#42c02e;
}
.setting .main .social-list .fa-qq{
    color: #3194d0;
}
.setting .main .social-list .fa-bug{
    color: #42c02e;
}
.setting .main .social-list .fa-google-plus{
    color: #ec6149;
}
.setting .save{
    width: 100px;
    margin: 30px 0 60px;
    border: none;
    border-radius: 20px;
    color: #fff;
    background-color: #42c02e;
    padding: 6px 12px;
    cursor: pointer;
}
</style>
