<template>
    <div class="cart">
         <!-- indicator-dots="{{indicatorDots}}"
            autoplay="{{autoplay}}"
            interval="{{interval}}"
            duration="{{duration}}" -->
        <swiper
        class="swiper"
           autoplay="true"
           indicator-dots="true"
           indicator-active-color="#fd5f2a"
           interval="2000"
           circular="true"

            >
            <block v-for="(item,index) in data" :key="index">
                <swiper-item>
                    <img :src="item" class="slide-image" mode="aspectFill"/>
                </swiper-item>
            </block>
        </swiper>
        <div style="color:#fd5f2a;height:50px;line-height:50px;padding:0 20px;">￥<span>99999999.00</span></div>
        <div style="font-size:20px;padding:0 20px;">产品图片</div>
       
        <ul >
            <li v-for="(item,index) in data" :key="index">
                <img :src="item" alt="" mode="aspectFill" class="shopDetialImg">
            </li>
        </ul>
        <div class="footer">
            <div class="shop">
                <img src="/static/tabs/home.png" alt="">
                <div>小店</div>
            </div>
            <div class="shopCart">
                 <img src="/static/tabs/card.png" alt="">
                <div>购物车</div>
            </div>
            <div class="add">加入购物车</div>
            <div class="buy">立即购买</div>
            
        </div>
    </div>
</template>

<script>
export default {
  data() {
    return {
      title: "购物车列表",
      data: [
        "http://img.palm-machinery.com/image/goods/detail/5aebd958c21be.jpg",
        "http://img.palm-machinery.com/image/goods/detail/5aebd958d3bb6.jpg",
        "http://img.palm-machinery.com/image/goods/detail/5aebd958edd20.jpg",
        "http://img.palm-machinery.com/image/goods/detail/5aebd9594b205.jpg",
        "http://img.palm-machinery.com/image/goods/detail/5aebd95916212.jpg",
        "http://img.palm-machinery.com/image/goods/detail/5aebd9592fe52.jpg",
        "http://img.palm-machinery.com/image/goods/detail/5aebd9596725d.jpg",
        "http://img.palm-machinery.com/image/goods/detail/5aebd959817d5.jpg",
        "http://img.palm-machinery.com/image/goods/detail/5aebd9599da29.jpg",
        "http://img.palm-machinery.com/image/goods/detail/5aebd959b8379.jpg"
      ]
    };
  },
  methods: {
    addCart() {
      console.log("添加购物车成功");
      wx.showModal({
        title: "确定添加购物车吗",
        content: "有钱人请确定,否则取消呗！！",
        success: function(res) {
          console.log(res);
          if (res.confirm) {
            wx.showToast({
              title: "添加购物车成功",
              icon: "none",
              duration: 1000
            });
          } else {
            wx.showToast({
              title: "你点击了取消",
              icon: "none",
              duration: 1000
            });
          }
        }
      });
    },
    goShopDetail(id) {
      wx.navigateTo({
        url: "/pages/logs/main"
      });
    }
  },
  onLoad(options) {
    // Do some initialize when page load.
    console.log(options);
    wx.showToast({
        title:`商品id为：${options.id}`,
    })
  },
  onReady() {
    // Do something when page ready.
    console.log("onReady");

  },
  onShow() {
    // Do something when page show.
    console.log("onShow");

  },
  onHide() {
    // Do something when page hide.
    console.log("onHide");
    
  },
  onUnload() {
    // Do something when page close.
    console.log("onUnload");

  },
  onPullDownRefresh() {
    // Do something when pull down.
    console.log("onPullDownRefresh");

  },
  onReachBottom() {
    // Do something when page reach bottom.
    console.log("onReachBottom");

  },
  onShareAppMessage() {
    // return custom share data when user share.
    console.log("onShareAppMessage");

  },
  onPageScroll() {
    // Do something when page scroll
    console.log("onPageScroll");

  }
};
</script>

<style scoped >
.cart {
  /* padding:60px 10px 0 10px; */
  background: #fafafa;
  padding-bottom: 60px;
}
.header {
  position: fixed;
  top: 0;
  left: 0;
  z-index: 2;
  width: 100%;
  height: 60px;
  line-height: 50px;
  font-size: 20px;
  font-weight: 600;
  background: #fff;
}
.shopListItem {
  display: flex;
  /* justify-content:space-around; */
  font-size: 16px;
  margin-bottom: 10px;
  background: #fff;
  padding-bottom: 10px;
  /* border-bottom: 0.5px solid #eee; */

  /* align-items: center; */
}
.shopImg {
  flex: none;
  width: 150px;
  height: 150px;
  margin-right: 20px;
}
.shopTitle {
  text-overflow: -o-ellipsis-lastline;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 1;
  -webkit-box-orient: vertical;
  align-content: center;
  margin-bottom: 20px;
}
.desc {
  font-size: 14px;
  color: #333;
  margin-bottom: 10px;
}
.clamp2 {
  text-overflow: -o-ellipsis-lastline;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  align-content: center;
}
.addCart {
  display: inline-block;
  border-radius: 10px;
  padding: 5px 10px;
  background: #f05b29;
  color: #fff;
}
.swiper {
  height: 375px;
}
.slide-image {
  width: 100%;
  height: 100%;
}
.shopDetialImg {
  width: 100%;
  height: 400px;
  /* height: auto; */
  display: block;
}

.footer {
  display: flex;
  position: fixed;
  width: 100%;
  bottom: 0;
  left: 0;
  background: #fff;
  text-align: center;
  font-size: 16px;
}
.shop,
.shopCart {
  flex: none;
  display: flex;
  flex-direction: column;
  justify-content: center;
  box-sizing: border-box;
  align-items: center;
  padding: 0 10px;
  color: #666;
  font-size: 12px;
}
.shop img,
.shopCart img {
  width: 20px;
  height: 20px;
  padding-bottom: 5px;
}

.add {
  background: #1a191e;
  height: 50px;
  line-height: 50px;
  flex: 1;
  color: #fff;
}
.buy {
  background: #f05b29;
  height: 50px;
  line-height: 50px;
  flex: 1;
  color: #fff;
}
</style>