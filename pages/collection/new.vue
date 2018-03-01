<template>
    <div>
        <my-header></my-header>
        <div class="my-container new-collection">
            <div class="row">
                <div class="col-8 main">
                    <h3>新建专题</h3>
                    <table>
                        <thead>
                        <tr>
                            <th class="settion-head"></th>
                            <th></th>
                        </tr>
                        </thead>
                        <tbody class="base">
                        <tr>
                            <td>
                                <div class="avatar-collection">
                                    <img src="../../assets/img/avatar-collection.png">
                                </div>
                            </td>
                            <td>
                                <a class="btn btn-hollow">
                                    <input type="file" class="hide" unselectable="on">
                                    上传专题封面
                                </a>
                            </td>
                        </tr>
                        <tr>
                            <td class="setting-title">
                                名称
                            </td>
                            <td>
                                <input name="nick-name" type="text"placeholder="填写名称，不超过50字">
                            </td>
                        </tr>
                        <tr>
                            <td class="setting-title pull-left setting-input">描述</td>
                            <td>
                                <textarea placeholder="填写描述"></textarea>
                            </td>
                        </tr>
                        <tr class="add-manager">
                            <td class="setting-title pull-left setting-input">其他管理员</td>
                            <td>
                                <div class="user-add">
                                    <input type="text" name="nick-name" placeholder="输入用户名">
                                </div>
                            </td>
                        </tr>
                        <tr>
                            <td class="setting-title setting-verticle">是否允许投稿</td>
                            <td>
                                <div class="col-4">
                                    <input @click="aa()" type="radio" name="push" value="true" ref="allow1" checked>
                                    <span>允许</span>
                                </div>
                                <div class="col-8">
                                    <input @click="aa()" type="radio" name="push" value="false" ref="allow2">
                                    <span>不允许</span>
                                </div>
                            </td>
                        </tr>
                        <tr :class={disabled:checkeds}>
                            <td class="setting-title setting-vertivle">投稿是否需要审核</td>
                            <td>
                                <div class="col-4">
                                    <input type="radio" name="verify" value="true" checked ref="xuyao1">
                                    <span>需要</span>
                                </div>
                                <div class="col-8">
                                    <input type="radio" name="verify" value="false" ref="xuyao2">
                                    <span>不需要</span>
                                </div>
                            </td>
                        </tr>
                        </tbody>
                    </table>
                    <div class="btn btn-success follow create">创建专题</div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    import myHeader from'~/components/myHeader'
    export default{
        data(){
            return{
                checkeds:false
            }
        },
        methods:{
           aa(){
               if(this.$refs.allow2.checked){
                   this.checkeds=true
                   this.$refs.xuyao1.disabled=true
                   this.$refs.xuyao2.disabled=true
               }else{
                   this.checkeds=false
                   this.$refs.xuyao1.disabled=false
                   this.$refs.xuyao2.disabled=false
               }
               console.dir(this.$refs.xuyao2)
           }
        },
        components: {
            myHeader
        }
    }
</script>
<style>
    input[type=radio]{
        margin: 4px 0 0;
    }
    .new-collection .row{
        padding-top:30px;
    }
    .new-collection .main{
        margin-bottom: 60px;
        margin-left: 12.5%;
    }
    .new-collection .main h3 {
        margin: 10px 0 20px;
        font-size: 21px;
        font-weight: 700;
        color: #333;
    }
    .new-collection .main table{
        width: 100%;
    }
    .new-collection .main td{
        padding:16px 0;
        font-size: 15px;
    }
    .new-collection .main .avatar-collection{
        cursor:default;
        width: 100px;
        height: 100px;
        margin-right: 50px;
    }
    .avatar-collection img{
        width: 100%;
        height: 100%;
        border:1px solid #ddd;
        border-radius: 10%;
    }
    .new-collection .main .btn-hollow{
        font-size: 14px;
        padding: 4px 12px;
    }
    .new-collection .main .btn-hollow:hover{
        background-color: #f5fcf3;
    }
    .new-collection .main .hide{
        position: absolute;
        display: block;
        width: 82px;
        opacity: 0;
    }
    .new-collection .main .setting-title{
        width: 150px;
        font-size: 15px;
        color:#969696;
    }
    .new-collection .main input[name=nick-name]{
        width: 100%;
    }
    .new-collection .main input{
        padding: 10px 15px;
        font-size: 15px;
        border:1px solid #c8c8c8;
        border-radius: 4px;
        background-color: rgba(181,181,181,0.098);
    }
    .new-collection .main .setting-input{
        line-height: 33px;
    }
    .new-collection .main textarea{
        width: 100%;
        height: 100px;
        margin-bottom: 10px;
        pdding:10px 15px;
        borber:1px solid #c8c8c8;
        border-radius: 4px;
        background-color: rgba(181,181,181,0.098);
        display: block;
        resize: none;
        outline-style: none;
    }
    .new-collection .main div.col-4,.new-collection .main div.col-8{
        float:left;
    }
    .new-collection .main span{
        margin: 0 5px 0 10px;
        font-size: 15px;
        color:#333;
        vertical-align: top;
    }
    .new-collection .main .create{
        margin: 20px 0 5px;
        border-radius: 20px;
    }
    .new-collection .main .disabled .setting-title{
        color:#ddd;
    }
    .new-collection .main .disabled span{
        color:#ddd;
    }
</style>