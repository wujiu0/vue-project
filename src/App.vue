<script>

import { defineComponent } from 'vue';;

export default defineComponent({
});
</script>

<template>
  <div id="app">
    <a-layout class="layout-wrapper">
      <a-layout-header
        class="layout-header"
        :style="{ position: 'fixed', zIndex: 1, width: '100%' }"
      >
        <div class="logo" />
        <a-menu
          theme="dark"
          mode="horizontal"
          :default-selected-keys="['2']"
          :style="{ lineHeight: '64px' }"
        >
          <a-menu-item key="1">nav 1</a-menu-item>
          <a-menu-item key="2">nav 2</a-menu-item>
          <a-menu-item key="3">nav 3</a-menu-item>
        </a-menu>
      </a-layout-header>
      <a-layout-content
        class="layout-main"
        :style="{ padding: '0 50px', marginTop: '64px' }"
      >
        <a-breadcrumb :style="{ margin: '16px 0' }">
          <a-breadcrumb-item>Home</a-breadcrumb-item>
          <a-breadcrumb-item>List</a-breadcrumb-item>
          <a-breadcrumb-item>App</a-breadcrumb-item>
        </a-breadcrumb>
        <div :style="{ background: '#fff', padding: '24px', minHeight: '380px' }">
          <router-view></router-view>
        </div>
      </a-layout-content>
      <a-layout-footer :style="{ textAlign: 'center' }">
        Ant Design ©2018 Created by Ant UED
      </a-layout-footer>
    </a-layout>
  </div>

</template>
<style scoped>
.layout-wrapper .logo {
  width: 120px;
  height: 31px;
  background: rgba(255, 255, 255, 0.2);
  margin: 16px 24px 16px 0;
  float: left;
}
.layout-header {
  height: 60px;
  line-height: 60px;
}
.layout-main {
  height: 100%;
}
</style>
