<template>
  <div class="com-sidebar-nav">
    <div class="title">VueUI-Widgets 组件列表</div>
    <ul>
      <li v-for="item in routeArray" :key="item">
        <router-link :to="item">{{item}}</router-link>
      </li>
    </ul>
  </div>
</template>
<script>
import { routeArray } from '../router'
export default {
  data() {
    return {
      routeArray
    }
  }
}
</script>
<style lang="less">
.com-sidebar-nav {
  padding-bottom: 30px;
  .title {
    padding: 0 12px;
    line-height: 48px;
    font-size: 15px;
    color: #1c2438;
    font-weight: bold;
  }
  ul {
    li {
      list-style: none;
      line-height: 36px;
      a {
        display: block;
        padding: 0 12px;
        font-size: 14px;
        &:hover {
          background-color: #f7f7f7;
        }
        &.router-link-active {
          background-color: #2d8cf0;
          color: #fff;
        }
      }
    }
  }
}
</style>