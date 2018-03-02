<template>
  <div>
   <my-header></my-header>
   <div class="setting my-container">
       <div class="row">
           <div id="aside" class=".aside col-4">
               <setting></setting>
           </div>
           <div class="main col-8">
              <table>
               <tbody>    
                  <tr>
                      <td class="top-line">
                          <div class="avatar">
                              <img src="/user.jpg" alt="">
                          </div>
                      </td>
                      <td class="top-line">
                          <a href="javascript:void(0)" class="hollow">
                              <input type="file" unselectable="on" class="hide">
                              更改头像
                          </a>
                      </td>
                  </tr>
                  <tr>
                      <td class="setting-title">昵称</td>
                      <td><input type="text" placeholder="请输入昵称" value="我是不和么"></td>
                  </tr>
                  <tr>
                      <td class="setting-title">电子邮件</td>
                      <td>
                          <form>
                             <input type="email" placeholder="请输入你的常用邮箱">
                             <button class="btn-hollow pull-right">发送</button>
                          </form>
                      </td>
                  </tr>
                  <tr>
                      <td class="setting-title">手机</td>
                      <td class="setted">
                          <div>132****8630</div>
                          <i class="fa fa-check"></i>
                          <span>已验证</span>
                          <a href="javascript:void(0)" class="cancel-bind">解除绑定</a>
                      </td>
                  </tr>
                  <tr>
                      <td class="setting-title">常用编辑器</td>
                      <td>
                          <div class="col-xs-4">
                              <input type="radio" value="plain" name="editor" checked>
                               <span>富文本</span>
                          </div>
                          <div class="col-xs-8">
                              <input type="radio" value="markdown" name="editor">
                               <span>
                                   Markdown
                                   <nuxt-link to="/p/123" class="help">
                                   <i class="fa fa-question-circle"></i>
                                   </nuxt-link>
                               </span>
                          </div>
                          <p>切换后对新建文章生效</p>
                      </td>
                  </tr>
                  <tr>
                    <td class="setting-title">语言设置</td>
                      <td>
                          <div class="col-xs-4">
                              <input type="radio" class="language" checked>
                               <span>中文简体</span>
                          </div>
                          <div class="col-xs-8">
                              <input type="radio" class="language">
                               <span>中文繁体</span>
                          </div>
                          </td>
                  </tr>
                  <tr>
                      <td class="setting-title">接收谁的简信</td>
                      <td>
                          <div class="col-xs-4">
                              <input type="radio" name="chat" checked>
                               <span>所有人</span>
                          </div>
                          <div class="col-xs-8">
                              <input type="radio" name="chat">
                               <span>我关注的人、我发过简信的人</span>
                          </div>
                          </td>
                  </tr>
                  <tr>
                       <td class="setting-title">提醒邮件通知</td>
                      <td>
                          <div class="col-xs-4">
                              <input type="radio" name="email" checked>
                              <span class="responsive-span">所有动态</span>
                          </div>
                          <div class="col-xs-4">
                                <input type="radio" name="email">
                              <span class="responsive-span">每天未读总汇</span>
                          </div>
                           <div class="col-xs-2">
                                 <input type="radio" name="email">
                              <span class="responsive-span">不接受</span>
                           </div>
                      </td>
                  </tr>
               </tbody>
              </table>
              <button class="save">保存</button>
           </div>
       </div>
   </div>
  </div>
</template>
<script>
import MyHeader from "~/components/myHeader";
import Setting from '~/components/Setting'
export default {
  name: "basic",
    mounted(){
      let value = document.querySelector('#aside ul .basic')
        value.className = 'asideActive'
    },
  components: {
    MyHeader,
    Setting
  }
};
</script>
<style scoped>
    .row{
        padding-top: 30px;
    }
.setting .main td {
  padding: 20px 0 20px 0px;
}
.setting .main tr {
  border-bottom: 1px solid #f0f0f0;
}
.setting .main tr:nth-of-type(1) {
  border: none;
}
.setting .main tr:last-child {
  border: none;
}
.setting .main .top-line {
  padding-top: 0;
}
.setting .main .avatar {
  width: 100px;
  height: 100px;
}
.setting .main .hollow {
  font-size: 14px;
  border: 1px solid rgba(59, 194, 29, 0.7);
  color: #42c02e !important;
  padding: 4px 12px;
  margin-left: 40px;
  font-weight: 400;
  text-align: center;
  background-color: #fff;
  border-radius: 40px;
  cursor: pointer;
}
.setting .main .btn-hollow {
  padding: 4px 12px;
  color: #42c02e !important;
  font-weight: 400;
  text-align: center;
  background-color: #fff;
  border-radius: 40px;
  cursor: pointer;
  border: 1px solid rgba(59, 194, 29, 0.7);
}
.setting .main .hide {
  position: absolute;
  width: 82px;
  opacity: 0;
}
.setting .main .setting-title {
  font-size: 15px;
  color: #969696;
}
.setting .main input[type="text"] {
  padding: 5px 10px;
  font-size: 15px;
  border: 1px solid #c8c8c8;
  border-radius: 4px;
  background-color: #f7f7f7;
}
.setting .main input[type="email"] {
  width: 70%;
  padding: 5px 10px;
  border: 1px solid #c8c8c8;
  border-radius: 4px;
  margin-right: 10px;
  background-color: #f7f7f7;
}
.setting .main .setted div {
  font-size: 15px;
  display: inline-block;
}
.setted i {
  margin-left: 10px;
  font-size: 12px;
  color: #969696;
  vertical-align: middle;
}
.setted span {
  margin-left: 3px;
  font-size: 14px;
  color: #969696;
}
.setted a {
  margin-left: 8px;
  font-size: 14px;
  color: #969696 !important;
}
input[type="radio"] {
  margin-top: 4px;
}
.setting .main span {
  margin: 0 20px 0 6px;
  font-size: 15px;
}
.setting .main .help {
  color: #969696 !important;
}
.setting .main p {
  padding-top: 15px;
  font-size: 12px;
  color: #969696;
}
.save {
  width: 100px;
  margin: 30px 0 60px 30px;
  border-radius: 20px;
  border: none;
  color: #fff;
  background-color: #42c02e;
  padding: 6px 12px;
  cursor: pointer;
}
table{
  width: 625px;
}

</style>
