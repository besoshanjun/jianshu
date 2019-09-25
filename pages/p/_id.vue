<template>
    <div @click="showMore=false">
        <my-header></my-header>
        <div class="note">
            <!--文章区域-->
            <div class="post">
                <!--正文1-->
                <div class="article">
                    <h1 class="title">月薪三千，就该去死吗？</h1>
                    <div class="author">
                        <nuxt-link class="avatar" to="/u/123">
                            <img src="../../assets/img/user.jpg">
                        </nuxt-link>
                        <div class="info">
                            <span class="name">测试用户</span>
                            <a href="javascript:void(0)" :class="followObj" @click="isFollow" @mouseover="noFollow"
                               @mouseleave="beFollow">
                                <i class="fa" :class="iconObj" ref="icon"></i>
                                <span ref="followWord">关注</span>
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
                    <div data-note-content="" class="show-content">
                        <p>01</p>
                        <p>昨晚我失眠了。</p>
                        <p>失眠的原因是看了电影《无问西东》，其中一个场景久久地萦绕于脑中：</p>
                        <p>吴岭澜是影中一位文学天赋极高但理科极差的学生。对于人生，他很少思考过，一味地随着大众的价值认知漂流。</p>
                        <p>当校长梅贻琦问他：“为什么不转去文学系？”时，他这样回答道：</p>
                        <p>“ 最好的学生都是学实科的。我只知道，这个年纪最重要的就是学习，何用管我学什么。每天把自己交给书本，心里就觉得踏实。”</p>
                        <p>梅贻琦答他：</p>
                        <p>“ 你还忽略了一件事，真实。人把自己置身于忙碌当中，有一种麻木的踏实，但丧失了真实。”</p>
                        <p>“什么是真实？”</p>
                        <p>“ 真实就是，你看什么，做什么，和谁在一起，有一种从心灵深处满溢出来的不懊悔、也不羞耻的平和与喜悦。”</p>
                        <p>
                            真实已经离我们多数人很远很远。不知从什么时候开始，“人生在世，名利二字”已经成为我们做人做事的行为标准，理想成为了一个人可以被嘲笑的代言词。若是一个人谈对他人的价值、对社会的奉献恐怕又会被扣上一顶“鸡汤”或“忽悠”的帽子。</p>
                        <p>做不了真实的自己，表达不了真实的自己，我们将原因归咎于现实。</p>
                        <p>
                            而那些越是父母受教育程度高、经济实力越强的家庭，为孩子未来的人生发展规划能规划出最优化最高效的路线，让他早日摆脱“现实”的束缚进而追求“真实”，境由心转，有更多时间思考自己想过的生活，有更多精力实现自己的价值。</p>
                    </div>
                    <div class="show-foot">
                        <nuxt-link to="/nb/123" class="notebook">
                            <i class="fa fa-book"></i>
                            <span>我的文集</span>
                        </nuxt-link>
                        <div class="copyright">
                            &copy;著作版权归作者所有
                        </div>
                    </div>
                    <div class="follow-detail">
                        <div class="info">
                            <nuxt-link class="avatar" to="/u/123">
                                <img src="../../assets/img/user.jpg" alt="">
                            </nuxt-link>
                            <a class="btn" href="javascript:void(0)" :class="followObj" @click="isFollow"
                               @mouseover="noFollow" @mouseleave="beFollow">
                                <i class="fa" :class="iconObj" ref="icon2"></i>
                                <span ref="followWord2">关注</span>
                            </a>
                            <nuxt-link class="title" to="/u/123">
                                测试用户
                            </nuxt-link>
                            <i class="fa fa-mars"></i>
                            <p>写了 46873 字， 被 26 人关注， 获得了 95 喜欢</p>
                        </div>
                        <div class="signature">
                            2018，田宝与你共同成长。
                            专注于自媒体写作，读书方法，时间管理，学习心得。
                            微信：tyh520zxc （欢迎畅聊）
                            微信公众号：田宝谈写作（内有大量免费学习资料与你分享）
                            田宝谈写作总目录：http://www.jianshu.com/p/59310bfe4210《普通人的写作进阶之道》
                            关于转载、授权等问题：请统一简信联系我的经纪人：南方有路：http://www.jianshu.com/u/6136f97e3f6e
                        </div>
                    </div>
                    <div class="meta-bottom">
                        <div class="like">
                            <div class="btn like-group" ref="like">
                                <div class="btn-like">
                                    <a href="javascript:void(0)" @click="isLike">
                                        <i class="fa fa-heart-o"></i>
                                        <span>喜欢</span>
                                    </a>
                                </div>
                                <div class="modal-wrap" ref="modal">
                                    <a href="javascript:void(0)">{{like_number}}</a>
                                </div>
                            </div>
                        </div>
                        <div class="share-group">
                            <a v-b-tooltip.hover title="分享到微信" href="javascript:void(0)">
                                <i class="fa fa-weixin weixin"></i>
                            </a>
                            <a v-b-tooltip.hover title="分享到微博" href="javascript:void(0)">
                                <i class="fa fa-weibo weibo"></i>
                            </a>
                            <a v-b-tooltip.hover title="分享到QQ" href="javascript:void(0)">
                                <i class="fa fa-qq qq"></i>
                            </a>
                            <a href="javascript:void(0)" class="more-share" @click.stop="showMore = true">
                                更多分享
                            </a>
                            <div class="more-share-model" v-if="showMore">
                                <ul>
                                    <li><a href="javascript:void(0)"><i class="fa qq">☆</i>分享到QQ空间</a></li>
                                    <li><a href="javascript:void(0)"><i class="fa fa-twitter twi"></i>分享到Twitter</a></li>
                                    <li><a href="javascript:void(0)"><i class="fa fa-facebook-official face"></i>分享到Facebook</a></li>
                                    <li><a href="javascript:void(0)"><i class="fa fa-google-plus goog"></i>分享到Google+</a></li>
                                    <li><a href="javascript:void(0)"><i class="fa dou">豆</i>分享到豆瓣</a></li>
                                </ul>
                                <div class="triangle"></div>
                            </div>
                        </div>
                    </div>
                </div>
                <!--回复组件-->
                <my-comment></my-comment>
            </div>
            <!--悬浮的操作框-->
            <div class="side-bar"></div>
            <!--对应的推荐阅读-->
            <div class="note-bottom"></div>
        </div>
    </div>
</template>
<script>
    import myHeader from '~/components/myHeader'
    import myComment from '~/components/myComment'
    export default{
        data(){
            return {
                followObj: {
                    'follow': true,
                    'following': false
                },
                iconObj: {
                    'fa-plus-square-o': true,
                    'fa-check': false
                },
                like: false,
                showMore:false,
                like_number:125
            }
        },
        components: {
            myHeader,
            myComment
        },
        methods: {
            isFollow: function () {
                let word = this.$refs.followWord.innerHTML;
                let word2 = this.$refs.followWord2.innerHTML;
                this.followObj.follow = !this.followObj.follow;
                this.followObj.following = !this.followObj.following;
                this.iconObj['fa-plus-square-o'] = !this.iconObj['fa-plus-square-o'];
                this.iconObj['fa-check'] = !this.iconObj['fa-check'];
                this.$refs.followWord.innerHTML = word == '关注' ? '已关注' : '关注';
                this.$refs.followWord2.innerHTML = word2 == '关注' ? '已关注' : '关注';
            },
            noFollow: function () {
                let word = this.$refs.followWord.innerHTML;
                if (word == '已关注') {
                    this.$refs.followWord.innerHTML = '取消关注';
                    this.$refs.followWord2.innerHTML = '取消关注';
                    this.$refs.icon.className = 'fa fa-close';
                    this.$refs.icon2.className = 'fa fa-close';
                }
            },
            beFollow: function () {
                let word = this.$refs.followWord.innerHTML;
                if (word == '取消关注') {
                    this.$refs.followWord.innerHTML = '已关注';
                    this.$refs.icon.className = 'fa fa-check';
                    this.$refs.followWord2.innerHTML = '已关注';
                    this.$refs.icon2.className = 'fa fa-check';
                }
            },
            isLike: function () {
                if (this.like == false) {
                    this.$refs.like.className = 'btn like-group active'
                    this.$refs.modal.className = 'modal-wrap live'
                    this.like_number = this.like_number + 1
                    this.like = !this.like
                } else {
                    this.$refs.like.className = 'btn like-group'
                    this.$refs.modal.className = 'modal-wrap'
                    this.like_number = this.like_number - 1
                    this.like = !this.like
                }
            }
        }
    }
</script>