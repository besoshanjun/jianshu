<template>
  <section>
    <div v-if="error.statusCode === 404">
      <div class="logo404">
        <img src="../assets/img/logo404.png">
      </div>
      <div class="page404">
        <img src="../assets/img/page404.jpg">
      </div>
      <div class="brief">
        <p>可能是因为您的链接地址有误、该文章已经被作者删除或转为私密状态。</p>
        <nuxt-link to="/" class="button btn btn-success">返回「简书」首页</nuxt-link>
      </div>
      <div></div>
    </div>
  </section>
</template>
<script>
export default {
    props: ['error']
}
</script>

<style scoped>
  @media (max-width:900px) {
    .logo404{
      display: none;
    }
    .page404{
      margin-top: 150px !important;
    }
  }
  .logo404{
    margin: 50px;
    width: 300px;
  }
  .page404 {
    width: 900px;
    margin: 20px auto 0;
  }
  .logo404 img,.page404 img{
    width: 100%;
  }
  .brief{
    margin-top: 50px;
    text-align: center;
  }
  .brief p{
    margin-top: 30px;
    font-size: 15px;
  }
  .brief .button{
    width: 200px;
    display: block;
    height: 50px;
    border-radius: 30px;
    line-height: 36px;
    margin: 50px auto 0 ;
  }
</style>
