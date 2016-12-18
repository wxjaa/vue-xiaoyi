<template>
<div class="" style="background-color:#fff">
  <h>
  </h>
  <div class="msg">
    {{msg2}}
  </div>
  <div class="container">
    <router-view></router-view>
  </div>
  <div style="width:100%;background-color:#eee">
    <div style="min-width:1200px;width:1200px;margin:20px auto 0">
      <foot></foot>
    </div>
  </div>
</div>
</template>

<script>
import h from './components/head.vue'
import foot from './components/footer.vue'
export default {
  data () {
    return {
      msg: '基于智能合约的数字资产OTC平台',
      msg2: '挂单 / 登录离线钱包'
    }
  },
  components: {
    h,
    foot
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
