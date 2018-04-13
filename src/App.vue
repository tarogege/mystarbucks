<template>
  <div id="app">
    <div class="row">
      <div class="left-wrapper">
        <leftnav @click.native="showMenu()" :menuShow="menuShow"></leftnav>
        <div class="leftmenu-wrapper" v-show="menuShow">
          <leftmenu class="left-menu"></leftmenu>
        </div>
        <div class="desc">
          <div v-show="!menuShow" class="desc-text">心情惬意，来杯咖啡吧</div>
        </div>
        <div class="group-btn">
          <a href="" class="btn login-btn"><span class="icon fa fa-user-o" aria-hidden="true"></span><span class="login-text">登录</span></a>
          <a href="" class="btn regist-btn">注册</a>
        </div>
        </div>
      <div class="right-wrapper">hhhh</div>
    </div>
  </div>
</template>

<script>
  import leftnav from './components/leftnav/leftnav.vue';
  import leftmenu from './components/leftmenu/leftmenu.vue';

export default {
  name: 'App',
  components: {
    leftnav: leftnav,
    leftmenu: leftmenu
  },
  data: function () {
    return {
      menuShow: false
    }
  },
  methods: {
    showMenu: function () {
      this.menuShow = !this.menuShow;
    }
  }
}
</script>

<style rel="stylesheet/stylus" lang="stylus">
  .row
    display flex
    .left-wrapper
      flex 0 0 450px
      .leftmenu-wrapper
        margin-left 30px
      .desc
        display table
        margin-left 30px
        height 100%
        .desc-text
          display table-cell
          padding-top 24px
          vertical-align bottom
          text-align center
          font-size: 16px
          font-weight 700
          padding-bottom 24px
      .group-btn
        margin-left 30px
        .login-btn
          color greenyellow
        .regist-btn
          margin-left 3px
          color black
          border-radius 13px
          border 1px solid green
    .right-wrapper
      flex 1
</style>
