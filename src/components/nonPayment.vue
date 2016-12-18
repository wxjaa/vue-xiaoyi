<template lang="html">
  <div class="row">
    <div class="col-sm-3 col-lg-3">
      <div id="left">
          <h4 class="left-title text-center">菜 单</h4>
          <ul>
            <li class="left-item" v-for="item in tips">
                 <router-link to="/#">{{item.text}}</router-link>
            </li>
          </ul>
      </div>
    </div>
    <div class="content col-sm-9 col-lg-9">
    <h3 class="h2" style="border-bottom:none">代付款订单</h3>
      <table class="table table-hover table-striped" style="margon-top:0;font-size:16px;">
        <thead>
          <tr style="background:#eee">
            <th class="font-b text-center">
              资产类型
            </th>
            <th class="font-b">
              购买数量
            </th>
            <th class="font-b">
              购买单价
            </th>
            <th class="font-b">
              总计 CNY
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
      <td class="text-justify">
       <button class="btn btn-primary order_btn" type="button" name="button">付 款</button>
       <button class="btn btn-primary order_btn" type="button" name="button">撤 单</button>
      </td>
    </tr>
   </tbody>
      </table>
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
  </div>
</div>
</template>

<script>
export default {
  data () {
    return {
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
  }
}
</script>

<style lang="css">
.font-b{
  font-weight: 500;
  font-family: "黑体"
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
.content>.table>tbody>tr>td,.content>.table>thead>tr>th{
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
