<template>
  <tab-bar>
    <tab-bar-item path="/home">
      <img slot="item-icon" src="../../../assets/img/tabbar/shouye.png" alt="">
      <div slot="item-text">首页</div>
    </tab-bar-item>
    <tab-bar-item path="/category">
      <img slot="item-icon" src="../../../assets/img/tabbar/leimupinleifenleileibie.png" alt="">
      <div slot="item-text">分类</div>
    </tab-bar-item>
    <tab-bar-item path="/cart">
      <img slot="item-icon" src="../../../assets/img/tabbar/qicheqianlian-.png" alt="">
      <div slot="item-text">购物车</div>
    </tab-bar-item>
    <tab-bar-item path="/profile">
      <img slot="item-icon" src="../../../assets/img/tabbar/biaoqianA01_wode-70.png" alt="">
      <div slot="item-text">我的</div>
    </tab-bar-item>
  </tab-bar>
</template>

<script>
  import TabBarItem from "components/common/tabbar/TabBarItem";
  import TabBar from "components/common/tabbar/TabBar";

  export default {
    name: "MainTabBar",
    components: {TabBarItem, TabBar}
  }
</script>

<style scoped>

</style>