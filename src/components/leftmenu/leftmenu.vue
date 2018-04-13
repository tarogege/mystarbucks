<template>
<div class="left-menu">
  <ul class="nav-list">
    <li v-for="item in navItems">{{item}}</li>
  </ul>
  <ul class="detail-list">
    <li v-for="item in detailItems">{{item}}</li>
  </ul>
</div>
</template>

<script type="text/ecmascript-6">
export default {
  data: function () {
    return {
      navItems: ['门店','我的账户','菜单'],
    detailItems: ['星巴克移动应用','星礼卡','星巴克甄选','咖啡星讲堂','上海烘培工坊','关于星巴克','帮助中心']
    };
  }
};
</script>

<style lang="stylus" rel="stylesheet/stylus">
.left-menu
  margin 0 20px
  .nav-list,.detail-list
    li
      font-size 16px
      font-weight 800
      padding-bottom 10px
      padding-top 10px
      &:last-child
        border-bottom 1px solid gray
</style>
