<template lang="html">
  <div id="tips">
<ol>
  <li v-for="item in items">
    {{item}}
  </li>
</ol>
  </div>
</template>

<script>
export default {
  data () {
    return {
      items: [
        '点击"浏览"按钮，找到钱包备份文件所在的硬盘位置，并导入。',
        '输入您在创建钱包时,设置的钱包密码。',
        '当前钱包页面为WED离线钱包页面，请放心导入钱包备份文件。（可通过断网验证）'
      ]
    }
  }
}
</script>

<style lang="css">
#tips{
  width:100%;
  margin-top:50px;
  background-color: #f2f2f2;
  padding:24px 20px 24px 0;
  line-height: 2;
  color:#aeaeae
}
</style>
