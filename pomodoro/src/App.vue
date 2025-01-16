<template>
  <v-app>
    <v-app-bar>
      <v-container class="d-flex align-center" style="background: lightgreen">
        <v-app-bar-title style="color: black">番茄鐘</v-app-bar-title>
        <v-btn prepend-icon="mdi-home" to="/" style="color: black">首頁</v-btn>
        <v-btn prepend-icon="mdi-format-list-bulleted" to="/list" style="color: black">事項</v-btn>
        <v-btn prepend-icon="mdi-cog" to="/settings" style="color: black">設定</v-btn>
      </v-container>
    </v-app-bar>
    <v-main style="background: orange">
      <!--
      slot = 插槽 = 自訂元件內的某個部分 HTML
      v-slot = "元件插槽提供的可用變數"
      Component = 目前路由應該顯示的元件
      -->
      <router-view v-slot="{ Component }">
        <!--
          keep-alive 包住的元件不會被銷毀
          include 指定保留的元件
          component = 動態元件
          is = 要使用的元件
        -->
        <keep-alive include="index">
          <component :is="Component"></component>
        </keep-alive>
      </router-view>
    </v-main>
  </v-app>
</template>
