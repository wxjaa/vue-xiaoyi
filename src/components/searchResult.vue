<template lang="html">
  <div class="row">
    <div class="msg">
      {{msg}} / <span style="color:#009cff">{{msg2}}</span>
    </div>
    <div class="col-sm-3 col-lg-3">
      <div id="tips">
    <ol>
      <li v-for="tip in tips">
        {{tip}}
      </li>
    </ol>
      </div>
    </div>
    <div class="content col-sm-9 col-lg-9">

      <form class="form-inline text-center" role="form" style="padding:20px 0;">
        <div class="form-group">
      <label  for="exampleInputEmail2">购买单价：</label>
      <input type="email" class="form-control" id="exampleInputEmail2" placeholder="请输入单价">
    </div>
        <div class="form-group">
      <label for="exampleInputEmail2">购买数量：</label>
      <input type="email" class="form-control" id="exampleInputEmail2" placeholder="请输入数量">
    </div>
        <div class="form-group">
      <label  for="exampleInputPassword2">总计</label>
      <span >0000.00</span>
    </div>
        <button type="submit" class="btn btn-primary">
          <router-link to="/login" style="color:#fff">去钱包结算</router-link>
        </button>
     </form>
        <table class="table table-hover table-striped" style="margon-top:0;font-size:16px;">
          <thead>
            <tr style="background:#eee">
              <th class="font-b text-center">
                小蚁股
              </th>
              <th class="font-b">
                数量
              </th>
              <th class="font-b">
                单价  CNY/股
              </th>
              <th class="font-b">
                总价
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
     <td>

     </td>
   </tr></tbody>
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
      tips: [
        '当您输入大于卖一价格是，将会优先与卖一挂单成交；卖一挂单数量不够时，再自动与卖二的订单成交。以此类推',
        '点击“去钱包结算”按钮后，请登录离线钱包尽快结算订单，否则可能会被他人抢先结算，导致订单无效。'
      ],
      msg: '集市',
      msg2: '小蚁股专区'
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
#tips{
  width:100%;
  margin-top:50px;
  background-color: #f2f2f2;
  padding:24px 20px 24px 0;
  line-height: 2;
  color:#aeaeae
}
</style>
