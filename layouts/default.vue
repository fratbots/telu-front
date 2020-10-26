<template>
  <el-container id="app">
    <el-header>
        <el-row>
          <el-col :span=4 class="logo">
            <Logo />
          </el-col>
          <el-col :span=20>
            <Menu />
          </el-col>
        </el-row>
    </el-header>
    <el-main>
      <Nuxt />
    </el-main>
    <el-footer class="footer">
      <Copyright />
    </el-footer>
  </el-container>
</template>

<style>
html {
  font-family: "Helvetica Neue",Helvetica,Arial,sans-serif;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  height: 100%;
}

body {
  height: 100%;
}

h1 {
  font-size: 48px;
  line-height: 1.3;
}

h2 {
  font-size: 36px;
  line-height: 1.3;
}

h3 {
  font-size: 28px;
  line-height: 1.3;
}

h4 {
  font-size: 22px;
  line-height: 1.3;
}

#__layout {
  height: 100%;
}

#__nuxt {
  height: 100%;
}

#app {
  min-height: 100%;
  display: grid;
  grid-template-rows: auto 1fr auto;
}
</style>

<style scoped>
.logo {
  display: flex;
  align-items: center;
  height: 60px;
}
</style>
