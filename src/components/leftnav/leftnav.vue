<template>
  <nav class="navbar">
    <div class="navbar-header">
      <div class="navbar-brand">
        <img src="./navbrand.png" width="49" height="40"/>
      </div>
    </div>

    <ul class="nav navbar-nav" v-show="!menuShow">
      <li v-for="item in navItems"><a href="" class="text">{{item}}</a></li>
    </ul>

    <button class="btn btn-link navbar-btn navbar-right">
      <i class="icon " aria-hidden="true" :class="iconChange"></i>
    </button>
  </nav>
</template>

<script type="text/ecmascript-6">
export default {
  data: function () {
    return {
      navItems: ['门店','我的账户','菜单'],
      navImg: '',
    };
  },
  props: {
    menuShow: {
      type: Boolean
    }
  },
  computed: {
    iconChange: function () {
      if (this.menuShow)
      {
        return 'fa fa-close';
      }else {
        return 'fa fa-align-justify';
      }
    }
  }
};
</script>

<style lang="stylus" rel="stylesheet/stylus">
.navbar
  display relative
  width 100%
  padding-right 30px
  .navbar-brand
    vertical-align top
    width 49px
    height 49px
    margin-right 12px
  .navbar-nav
    vertical-align top
    padding-top 10px
    font-size 16px
    font-weight 800
    .text
      color black
  .btn
    display absolute
    top 0px
    right 0
    .icon
      padding-top 13px
      color black
      font-size 16px
</style>
