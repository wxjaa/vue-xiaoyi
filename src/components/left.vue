<template lang="html">
  <div id="left">
      <h4 class="left-title text-center">菜 单</h4>
      <ul>
        <li class="left-item" v-for="item in items">
             <router-link to="item.router">{{item.text}}</router-link>
        </li>
      </ul>
  </div>
</template>

<script>
export default {
  data () {
    return {
      items: [{
        text: '我 的 挂 单',
        router: ''
      }, {
        text: '代 付 款',
        router: ''
      }, {
        text: '资 产 列 表',
        router: ''
      }, {
        text: '个 人 中 心',
        router: ''
      }, {
        text: '隐 私 政 策',
        router: ''
      }, {
        text: '关 于',
        router: ''
      }]
    }
  }
}
</script>

<style lang="css">
#left{
  width:100%;
  margin-top:30px;
  padding:24px 0;

}
.left-title{
  width:100%;
line-height: 2;
background-color: #009cff;
color:#fff;
margin-bottom: 0;
word-spacing: 50px;
font-size: 22px;
}
#left>ul{
  margin:0px !important;
  padding:0;
}
.left-item{
  width: 100;
  background-color: #f2f2f2;
  margin-top: 4px;
  list-style: none;
  padding:10px 0 10px 70px;
  font-size: 16px;
}
.left-item>*{
  color:#939393;

}
</style>
