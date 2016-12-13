<template>
<div class="" style="background-color:#fff">
  <h>
  </h>
  <div class="msg">
    {{msg}}
  </div>
  <div class="container">
    <div class="col-sm-3">
       <tips></tips>
    </div>
    <div class="col-sm-9">
      <router-view></router-view>
      <login></login>
    </div>
  </div>
</div>
</template>

<script>
import h from './components/head'
import login from './components/login'
import tips from './components/tips'
export default {
  name: 'app',
  data () {
    return {
      msg: '挂单 / 登录离线钱包'
    }
  },
  components: {
    h,
    login,
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
</style>
