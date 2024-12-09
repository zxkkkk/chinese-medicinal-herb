<template>
  <div class="container">
    <!-- Navigation -->
    <div class="navigation">
      <div class="nav-item" v-for="item in navItems" :key="item.name">
        <i :class="'iconfont ' + item.iconClass"></i>
        <span>{{ item.name }}</span>
      </div>
    </div>

    <!-- Divider -->
    <div class="divider">
      <span class="divider-text">草药</span>
    </div>

    <!-- Content -->
    <div class="content">
      <div class="category" v-for="category in categories" :key="category">
        {{ category }}
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'Index',
  data() {
    return {
      navItems: [
        { name: '搜索', iconClass: 'icon-sousuo' },
        { name: '草药', iconClass: 'icon-zhongcaoyaojidi' },
        { name: '植物', iconClass: 'icon-zhiwu' },
        { name: '药方', iconClass: 'icon-caoyaofang1' },
        { name: '性味', iconClass: 'icon-zhishideng-green' },
        { name: '典籍', iconClass: 'icon-a-05-jingdianyaofang' },
        { name: '方剂', iconClass: 'icon-fangjiku' },
        { name: '功效', iconClass: 'icon-zhishideng-green' },
      ],
      categories: [
        '动物类',
        '花类',
        '果实/种子类',
        '根茎类',
        '藤木类',
        '枝叶/树皮类',
        '矿物类',
        '叶类',
        '皮类',
        '菌藻类',
        '树脂类',
        '其他类',
      ],
    }
  },
})
</script>

<style scoped>
.navigation {
  background-color: white;
  display: flex;
  justify-content: space-around;
  padding: 10px 0;
  margin-top: 10px;
}

.nav-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  color: gray;
}

.iconfont {
  font-size: 24px;
  margin-bottom: 5px;
}

.divider {
  height: 1px;
  background-color: #ccc;
  margin: 20px 15px;
  position: relative;
  text-align: center;
}

.divider-text {
  position: absolute;
  top: -10px;
  background: white;
  padding: 0 10px;
  color: gray;
  font-size: 14px;
}

.content {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  padding: 10px;
  margin-top: 20px;
}

.category {
  background-color: #e6e8ff;
  color: black;
  padding: 10px 30px;
  margin: 5px;
  border-radius: 10px;
  text-align: center;
  border: 2px solid #c8baf0;
  flex: 1 1 20%;
}
.category:hover {
  background-color: #d7d2f6; /* 悬停时的背景颜色 */
}
</style>
