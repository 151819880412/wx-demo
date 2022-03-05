<template>
  <div class='firstViewContainer'>
    <swiper @change="handleChange" :indicator-dots="index!==3" indicator-color="pink" indicator-active-color="green" circular="false">
      <swiper-item>
        <img src="/static/images/user.png" alt="">  
      </swiper-item> 
      <swiper-item>
        <img src="/static/images/user.png" alt="">  
      </swiper-item> 
      <swiper-item>
        <img src="/static/images/user.png" alt="">  
      </swiper-item> 
      <swiper-item>
        <img src="/static/images/user.png" alt="">  
      </swiper-item> 
    </swiper>
    <button @click="toIndex" class="btn" v-show="index==3">开始体验</button>
  </div>
</template>
<script>
export default {
  name: '',
  props: {},
  data() {
    return {
      index:0,
    };
  },
  created() {},
  mounted() {},
  computed: {},
  methods: {
    handleChange(event){
      console.log(event.mp.detail.current)
      // 更新index的值
      this.index = event.mp.detail.current
    },
    toIndex(){
      // 跳转至index页面
      wx.navigateTo({
        url:"/pages/index/main"
      })
    }
  },
  watch: {},
  components: {},
  beforeDestroy() {}
};
</script>
<style >

.firstViewContainer{
  height: 100%;
}
.firstViewContainer swiper{
  width: 100%;
  height: 100%;
}
.firstViewContainer swiper img{
  width: 100%;
  height: 100%;
}
</style>