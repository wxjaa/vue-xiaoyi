<template>
<div class="" style="background-color:#fff">
  <div id="head" style="background-color:#eee">
    <div class="logo">
      <img src="./assets/logo.png" alt="" />
      <span id="des">{{ msg }}</span>
    </div>
    <nav class="navbar navbar-default" role="navigation">
      <div class="container-fluid">
        <!-- Collect the nav links, forms, and other content for toggling -->
        <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
          <ul class="nav navbar-nav">
            <li class="frist ">
              <a class="menu">
                <router-link to="/home">分类资产</router-link>
              </a>
            </li>
            <li>
              <a class="menu">
                <router-link to="/home">首 &nbsp 页</router-link>
              </a>
            </li>
            <li>
              <a class="menu">
                <router-link to="/home">免费挂单</router-link>
              </a>
            </li>
            <li>
              <a class="menu">
                <router-link to="/home">发 &nbsp 现</router-link>
              </a>
            </li>
          </ul>
          <form class="navbar-form navbar-left" role="search">
            <div class="form-group">
              <input type="text" class="form-control" placeholder="小蚁股">
            </div>
            <button type="submit" class="btn btn-default">搜索</button>
          </form>
        </div>
        <!-- /.navbar-collapse -->
      </div>
      <!-- /.container-fluid -->
    </nav>
  </div>
  <div class="msg">
    {{msg2}}
  </div>
  <div class="container">
    <div class="col-sm-3">
      <tips></tips>
    </div>
    <div class="col-sm-9">
      <router-view></router-view>
    </div>
  </div>
  <div class="" style="width:100%;background-color:#eee">
    <div style="min-width:1200px;width:1200px;margin:20px auto 0">
      <div class="" id="footer">
        <div class="row foot-top">
          <div class="col-lg-3 col-md-3 bg-li">
            <span class="bg-blue  bg-blue1">
              </span>
            <div class="foot-li" style="">
              <p class="foot-type">资金无忧</p>
              <p class="foot-des">智能合约点对点结算</p>
            </div>
          </div>
          <div class="col-lg-3 col-md-3 bg-li">
            <span class="bg-blue  bg-blue2">
              </span>
            <div class="foot-li" style="">
              <p class="foot-type">快捷撮合</p>
              <p class="foot-des">无确认的信息撮合效率</p>
            </div>
          </div>
          <div class="col-lg-3 col-md-3 bg-li">
            <span class="bg-blue bg-blue3">
              </span>
            <div class="foot-li" style="">
              <p class="foot-type">免费挂单</p>
              <p class="foot-des">无需实名，一键挂单</p>
            </div>
          </div>
          <div class="col-lg-3 col-md-3 bg-li" style="background-image:none">
            <span class="bg-blue bg-blue4">
              </span>
            <div class="foot-li" style="">
              <p class="foot-type">海量品类</p>
              <p class="foot-des">满足长尾市场投资需求</p>
            </div>
          </div>
        </div>
        <div class="row">
          <div class="col-lg-12 col-md-12">
            <div class="row about">
              <div class="col-lg-10 col-md-10  row">
                <div class="col-lg-3  col-md-3 text-center">
                  <h4 class="text-color text-type2">合作伙伴</h4>
                  <ul class="list-unstyled">
                    <li>
                      <router-link class="text-color2" to="/time-entries">小蚁区快链</router-link>
                    </li>
                    <li>
                      <router-link class="text-color2" to="/time-entries">评级公司</router-link>
                    </li>
                    <li>
                      <router-link class="text-color2" to="/time-entries">众筹平台</router-link>
                    </li>
                    <li>
                      <router-link class="text-color2" to="/time-entries">巴比特</router-link>
                    </li>
                  </ul>
                </div>
                <div class="col-lg-3 col-md-3 text-center">
                  <h4 class="text-color text-type2">了解我们</h4>
                  <ul class="list-unstyled">
                    <li>
                      <router-link class="text-color2" to="/time-entries">了解小蚁</router-link>
                    </li>
                    <li>
                      <router-link class="text-color2" to="/time-entries">什么是OTC</router-link>
                    </li>
                    <li>
                      <router-link class="text-color2" to="/time-entries">OTC优势</router-link>
                    </li>
                    <li>
                      <router-link class="text-color2" to="/time-entries">联系我们</router-link>
                    </li>
                  </ul>
                </div>
                <div class="col-lg-3 col-md-3 text-center">
                  <h4 class="text-color text-type2">帮助中心</h4>
                  <ul class="list-unstyled">
                    <li>
                      <router-link class="text-color2" to="/time-entries">投资流程</router-link>
                    </li>
                    <li>
                      <router-link class="text-color2" to="/time-entries">挂单流程</router-link>
                    </li>
                    <li>
                      <router-link class="text-color2" to="/time-entries">客服中心</router-link>
                    </li>
                    <li>
                      <router-link class="text-color2" to="/time-entries">常见问题</router-link>
                    </li>
                  </ul>
                </div>
                <div class="col-lg-3 col-md-3 text-center">
                  <h4 class="text-color text-type2">友情链接</h4>
                  <ul class="list-unstyled">
                    <li>
                      <router-link class="text-color2" to="/time-entries">小蚁官网</router-link>
                    </li>
                    <li>
                      <router-link class="text-color2" to="/time-entries">BB评级</router-link>
                    </li>
                    <li>
                      <router-link class="text-color2" to="/time-entries">天使汇</router-link>
                    </li>
                    <li>
                      <router-link class="text-color2" to="/time-entries">比特时代</router-link>
                    </li>
                  </ul>
                </div>
              </div>
              <div class="col-lg-2 text-center">
                <h4 class="text-color text-type2">微信订阅号</h4>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
import tips from './components/tips'
export default {
  data () {
    return {
      msg: '基于智能合约的数字资产OTC平台',
      msg2: '挂单 / 登录离线钱包'
    }
  },
  components: {
    tips
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.logo {
  width: 1200px;
  margin: 0 auto;
  padding-left: 20px;
}

.logo>img {
  margin: 0 10px 0 50px;
}

.navbar {
  background-color: #000 !important;
  border: none !important;
}

.container-fluid {
  width: 1200px;
  margin: 0 auto;
}

.nav {
  width: 65%;
}

ul>.frist {
  background: url(assets/ver-line.png) no-repeat left center;
}

ul>li>.menu {
  color: #fff !important;
  font-size: 1.2em;
  background: url(assets/ver-line.png) no-repeat right center;
  padding-left: 30px !important;
  padding-right: 30px !important;
}

.menu>a {
  color: inherit;
}

.search {
  display: inline-block;
}

#des {
  display: inline-block;
  height: 100%;
  line-height: 100%;
  font-weight: 500;
  font-size: 1.2
}

.container {
  height: 600px;
}

.container>div {
  height: 100%;
}

.msg {
  background-color: #f2f2f2;
  margin: 10px auto;
  width: 1200px;
  padding: 10px;
  border-radius: 6px;
}

.foot-top {
  padding: 20px 0;
  margin: 0;
  border-bottom: 1px solid #e2e2e2
}

.bg-blue {
  background-color: #009cff;
  width: 50px;
  height: 50px;
  display: inline-block;
  border-radius: 6px;
  background-position: center;
  background-repeat: no-repeat;
}

.bg-blue1 {
  background-image: url(assets/foot-1.png);
}

.bg-blue2 {
  background-image: url(assets/foot-2.png);
}

.bg-blue3 {
  background-image: url(assets/foot-3.png);
}

.bg-blue4 {
  background-image: url(assets/foot-4.png);
}

.foot-top p {
  margin: 0;
}

.foot-li {
  display: inline-block;
  font-family: '黑体';
  padding-left: 12px;
  vertical-align: top;
  padding-top: 4px;
}

.bg-li {
  background: url(assets/ver-line2.png) right center no-repeat;
}

.foot-type {
  font-size: 22px;
  font-weight: 600;
  line-height: 1;
  padding-bottom: 5px
}

.foot-des {
  font-size: 20px;
  color: #5f5f5f;
  line-height: 1
}

.list-unstyled>li {
  width: 100%;
  padding-left: 75px;
  text-align: left;
}

.text-color {
  color: #666 !important
}

.text-color2 {
  color: #9d9d9d !important
}

.text-type2 {
  font-family: "黑体"
}
</style>
