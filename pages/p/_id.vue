<template>
    <div>
        <my-header></my-header>
        <div class="note">
            <!--文章区域-->
            <div class="post">
                <!--正文-->
                <div class="article">
                    <h1 class="title">月薪三千，就该去死吗？</h1>
                    <div class="author">
                        <nuxt-link class="avatar" to="/u/123">
                            <img src="../../assets/img/user.jpg">
                        </nuxt-link>
                        <div class="info">
                            <span class="name">测试用户</span>
                            <a href="javascript:void(0)" ref="a" class="btn-sm follow" @click="btnPay" @mouseover="over" @mouseleave="out">
                                <i ref="payi" class="fa fa-plus-square-o"></i>
                                <span ref="pay">关注</span>
                            </a>
                            <div class="meta">
                                <span>2018.01.23 16:09</span>
                                <span>字数 2273</span>
                                <span>阅读 882</span>
                                <span>评论 7</span>
                                <span>喜欢 34</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <!--炫富的操作框-->
            <div class="side-bar"></div>
            <!--对应的推荐阅读-->
            <div class="note-bottom"></div>
        </div>
    </div>
</template>
<script>
    import myHeader from '~/components/myHeader'
    export default{
        data(){
            return{
                pay:true
            }
        },
        components:{
            myHeader
        },
        methods:{
            btnPay(){
                if(this.pay){
                    this.$refs.pay.innerText ='已关注'
                    this.$refs.payi.className='fa fa-check'
                    this.$refs.a.className = 'btn-sm notfollow'
                    this.pay = !this.pay
                }else{
                    this.$refs.pay.innerText = '关注'
                    this.$refs.payi.className='fa fa-plus-square-o'
                    this.$refs.a.className ='btn-sm follow'
                    this.pay = !this.pay
                }
            },
            over(){
                if(!this.pay){
                    this.$refs.pay.innerText ='取消关注'
                    this.$refs.payi.className='fa fa-close'
                }
            },
            out(){
                if(!this.pay){
                    this.$refs.pay.innerText ='已关注'
                    this.$refs.payi.className='fa fa-check'
                }
            }
        }
    }
</script>