<template lang="html">
  <div class="row">
    <div class="msg">
      {{msg}}
    </div>
    <div class="col-sm-3 col-lg-3">
      <div id="left">
          <h4 class="left-title text-center">菜 单</h4>
          <ul>
            <li class="left-item" v-for="tip in tips">
              <router-link to="/#">{{tip.text}}</router-link>

            </li>
          </ul>
      </div>
    </div>
  <div class="content col-sm-9 col-lg-9" v-on:click="hide">
    <h3 class="h2" style="border-bottom:none">账户总资产估算：{{price}} &nbsp;CNY</h3>
      <table class="table table-hover table-striped" style="margon-top:0;font-size:16px;">
        <thead>
          <tr style="background:#eee">
            <th class="font-b text-center">
              资产类型
            </th>
            <th class="font-b">
              总量
            </th>
            <th class="font-b">
            冻结量
            </th>
            <th class="font-b">
              可用量
            </th>
            <th class="font-b">

            </th>
          </tr>
        </thead>
   <tbody>
     <tr>

     </tr>
  <tr v-for="item in items">
   <td class="text-center">
     {{item.type}}
   </td>
   <td>
     {{item.num}}
   </td>
   <td>
     {{item.price}}
   </td>
   <td>
     {{item.total}}
   </td>
   <td class="">
     <button class="btn btn-primary order_btn" v-on:click="show" type="button" name="button">出 售</button>

   </td>
 </tr></tbody>
      </table>
      <div v-if="isSend_sell" class="send_sellPop">
           <h2 style="margin-top:0;">挂单成功!</h2>
           <p>
             可在“我的挂单”中查看详情。
           </p>
      </div>
      <div v-if="isSell" class="sell_pop">
        <div class="sell_content">
          <div id="sanjiao">

          </div>
          <form class="form-horizontal" role="form">
    <div class="form-group">
      <span for="inputEmail3" class="col-sm-4 text-justify control-label sell_info">资产类型：<span class="left_fix">&nbsp;</span></span>
      <div class="col-sm-8 p-l0" style="padding-top:7px;">小蚁股</div>
    </div>
    <div class="form-group">
      <span for="inputEmail3" class="col-sm-4 text-justify control-label sell_info">可用量：<span class="left_fix">&nbsp;</span></span>
      <div class="col-sm-8 p-l0" style="padding-top:7px;">2382</div>
    </div>
    <div class="form-group">
      <span for="inputEmail3" class="col-sm-4 text-justify control-label sell_info">市场价：<span class="left_fix">&nbsp;</span></span>
      <div class="col-sm-8 p-l0" style="padding-top:7px;">0.88 CNY</div>
    </div>
    <div class="form-group">
        <span for="inputEmail3" class="col-sm-4 text-justify control-label sell_info">出售量：<span class="left_fix">&nbsp;</span></span>
      <div class="col-sm-8 p-l0">
        <input type="number" class="form-control" id="sellNUm" placeholder="请输入数量">
      </div>
    </div>
    <div class="form-group">
        <span for="inputEmail3" class="col-sm-4 text-justify control-label sell_info">出售价：<span class="left_fix">&nbsp;</span></span>
      <div class="col-sm-8 p-l0">
        <input type="number" class="form-control" id="sellNUm" placeholder="请输入价格">
      </div>
    </div>
    <div class="form-group" style="padding-top:20px;margin-top:30px;border-top:1px solid #d1d1d1">
      <div class="col-sm-offset-8 col-sm-4">
        <button type="button" class="btn btn-primary" v-on:click="showPop">发送卖单</button>
      </div>
    </div>
  </form>
        </div>
      </div>
      <p class="tips">
        离线钱包有小蚁区块链提供技术支持
      </p>
      <nav>
  <ul class="pagination order_page pagination-sm">
    <li><a href="#">&laquo;</a></li>
    <li><a href="#">1</a></li>
    <li><a href="#">2</a></li>
    <li><a href="#">3</a></li>
    <li><a href="#">4</a></li>
    <li><a href="#">5</a></li>
    <li><a href="#">&raquo;</a></li>
  </ul>
</nav>
  </div></div>
</template>

<script>
export default {
  data () {
    return {
      price: '11000.75',
      msg: '你已登录离线钱包',
      isSell: false,
      isSend_sell: false,
      items: [{
        type: '小蚁股',
        num: '10000.25',
        price: '0.95',
        total: '95000'
      }, {
        type: '小蚁币',
        num: '236.00',
        price: '1.05',
        total: '95000'
      }],
      tips: [{
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
  },
  methods: {
    show: function (e) {
      e = e || window.event
      e.stopPropagation()
      e.preventDefault()
      this.isSell = !this.isSell
    },
    hide: function (e) {
      e = e || window.event
      e.stopPropagation()
      e.preventDefault()
      this.isSell = false
      this.isSend_sell = false
    },
    showPop: function (e) {
      e = e || window.event
      e.stopPropagation()
      e.preventDefault()
      this.isSell = false
      this.isSend_sell = true
    }
  }
}
</script>

<style lang="css">
.font-b{
  font-weight: 500;
  font-family: "黑体"
}
.p-l0{
  padding-left: 0 !important;
}
.btn-primary{
  background: #009cff !important;
  border-color: #009cff !important
}
.order_btn{
  padding:10px;
  word-spacing: 8px;
  font-size: 18px !important;
  margin-right:30px;
}
.content>.table>tbody>tr>td,.content>.table>thead>tr>th,.sell_content .table>tbody>tr>td{
  vertical-align: middle;
}
.content>.table>tbody>tr>td:not(:last-child),.content>.table>thead>tr>th:not(:last-child){
  padding:8px 35px;
}
.order_page{
  position:absolute;
  bottom: 120px;
  right:10px;
}
/*.text-justify{
  text-align: justify !important;
}*/
.sell_pop{
  position:absolute;
  top:85px;
  right:178px;
  box-shadow: 0 0 25px #666;
  width:350px;
  background: #fff;
  z-index: 999;
}
.send_sellPop{
  position:absolute;
  top:120px;
  right:178px;
  background: #fff;
  z-index: 999;
  padding: 30px;
  font-size: 16px;
  line-height: 1.6;
  color:#666;
    box-shadow: 0 0 25px #666;
}
.sell_content{
  position:relative;
  padding: 25px;
  padding-bottom: 0;
  font-size: 16px;
  color:#666;
}
.sell_content .control-label{
  padding-left: 0 !important;
  padding-right: 0 !important
}
/*.sell_info{
  display: inline-block;
}*/
#sanjiao{
  width:30px;
  height:30px;
  background-color:#fff;
  /*box-shadow:8px -8px 8px #666;*/
  position:absolute;top:30px;
  right:-14px;
  z-index: 990;
  transform:rotate(45deg);
-ms-transform:rotate(45deg); 	/* IE 9 */
-moz-transform:rotate(45deg); 	/* Firefox */
-webkit-transform:rotate(45deg); /* Safari 和 Chrome */
-o-transform:rotate(45deg); 	/* Opera */

}
.justify_fix{display:inline-block; width:100%; height:0; overflow:hidden;}
</style>
