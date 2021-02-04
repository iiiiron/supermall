<template>
  <div id="home">
    <nav-bar class="home-nav"><div slot="center">购物街</div></nav-bar>
    <swiper>
      <swiper-item v-for="item in banners">
        <a :href="item.link">
          <img :src="item.image" alt="">
        </a>
      </swiper-item>

    </swiper>
  </div>

</template>

<script>
  import NavBar from "../../components/common/navbar/NavBar";
  import {getHomeMutidata} from "../../network/home";
  // import HomeSwiper from "./childComps/HomeSwiper";
  import {Swiper,SwiperItem} from 'components/common/swiper'

  export default {
    name: "Home",
    components:{
      // HomeSwiper,
      NavBar,
      Swiper,
      SwiperItem
    },
    data(){
      return {
        banners:[],
        recommends:[]
      }
    },
    created() {
      //1.请求多个数据
      getHomeMutidata().then(res => {
        // this.result = res;
        this.banners = res.data.banner.list
        this.recommends = res.data.recommend.list
      })
    }
  }
</script>

<style scoped>
  .home-nav{
    background-color: var(--color-tint);
    color:#fff;
  }

</style>