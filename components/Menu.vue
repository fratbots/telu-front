<template>
  <el-menu mode="horizontal" :default-active="$route.path">
    <el-menu-item index="/reader">
      <nuxt-link to="/reader" class="link">
        Start a Journey
      </nuxt-link>
    </el-menu-item>
    <el-menu-item index="/author">
      <nuxt-link to="/author" class="link">
        Become an Author
      </nuxt-link>
    </el-menu-item>
  </el-menu>
</template>

<style scoped>
.link {
  display: inline-block;
  height: 100%;
}
</style>
