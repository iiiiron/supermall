<template>
  <div class="tab-bar-item" @click="itemClick">
    <slot name="item-icon"></slot>
    <slot name="item-text"></slot>
<!--    <img src="../../assets/img/shouye.png" alt="">-->
<!--    <div>首页</div>-->
  </div>
</template>

<script>
  export default {
    name: "TabBarItem",
    props:{
      path: String
    },
    methods:{
      itemClick(){
        this.$router.replace(this.path).catch(err => err)
        // console.log('itemclick');
      }
    }
  }
</script>

<style scoped>
  .tab-bar-item{
    flex: 1;
    text-align: center;
    height: 49px;
    font-size: 14px;
    color: black;
  }
  .tab-bar-item img{
    width:24px;
    height: 24px;
    margin-top: 3px;
    vertical-align: middle;
  }
</style>