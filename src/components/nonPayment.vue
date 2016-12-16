<template lang="html">
  <div class="content">
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
</style>
