<template>
  <view class="detail-container">
    <!-- 轮播图 -->
    <swiper class="swiper-container" :autoplay="true" :interval="3000" :duration="500" circular>
      <swiper-item v-for="(item, index) in images" :key="index">
        <image class="swiper-image" :src="item" mode="aspectFill"></image>
      </swiper-item>
    </swiper>

    <!-- 用户信息和操作 -->
    <view class="user-action">
      <button class="upload-button" size="mini" plain type="primary">上传</button>
      <button class="favorite-button" size="mini" plain type="warn">加入收藏</button>
    </view>

    <!-- 描述 -->
    <view class="description">
      <text>
        桑螵蛸, 蜱蛸, 桑蛸, 冒焦, 螵蛸, 致神, 螳蛸子, 桑上螳蛸窠, 野狐鼻涕, 赖尿郎, 刀螂子,
        老鸹芯脐, 螳蛸蛋, 尿唧唧, 流尿狗, 猴儿包, 螳蛸壳, 螳蛸子, 刀螂子, 螳蛸蛋, 桑蛸, 螵蛸, 猴儿包
      </text>
    </view>

    <!-- 分类 -->
    <view class="classification">
      <text>【分类】动物类</text>
    </view>

    <!-- 性味 -->
    <view class="taste">
      <text>【性味】甘、咸，平。</text>
    </view>

    <!-- 性质 -->
    <view class="property">
      <text>【性质】咸甘，平。</text>
    </view>
  </view>
</template>

<script setup>
import { ref } from 'vue'

const images = ref([
  '/static/images/image1.jpg',
  '/static/images/image2.jpg',
  '/static/images/image3.jpg',
  // 更多图片路径...
])
</script>

<style lang="scss" scoped>
.detail-container {
  padding: 20rpx;
  .swiper-container {
    height: 300rpx;
    .swiper-image {
      width: 100%;
      height: 100%;
    }
  }
  .user-action {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10rpx 0;
    .username {
      font-size: 28rpx;
      color: #888;
    }
    .upload-button,
    .favorite-button {
      margin-left: 20rpx;
      color: #fff;
    }
    .upload-button {
      background-color: #007aff;
    }
    .favorite-button {
      background-color: #ff9500;
    }
  }
  .description,
  .classification,
  .taste,
  .property {
    margin: 20rpx 0;
    padding: 10rpx;
    background-color: #f9f9f9;
    border-radius: 10rpx;
  }
}
</style>
