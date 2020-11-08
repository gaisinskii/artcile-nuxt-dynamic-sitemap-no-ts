<template>
  <div>
    <el-header class="the-header">
      <nav class="the-header__nav">
        <nuxt-link class="the-header__link" :to="{ name: 'index' }">
          <el-button plain> Home Page </el-button>
        </nuxt-link>
        <nuxt-link class="the-header__link" :to="{ name: 'users' }">
          <el-button plain> All Users </el-button>
        </nuxt-link>
        <nuxt-link class="the-header__link" :to="{ name: 'albums' }">
          <el-button plain> All Albums </el-button>
        </nuxt-link>
        <nuxt-link class="the-header__link" :to="{ name: 'todos' }">
          <el-button plain> All Todos </el-button>
        </nuxt-link>
        <nuxt-link class="the-header__link" :to="{ name: 'exclude-one' }">
          <el-button plain> Exclude Page #1 </el-button>
        </nuxt-link>
        <nuxt-link class="the-header__link" :to="{ name: 'exclude-two' }">
          <el-button plain> Exclude Page #2 </el-button>
        </nuxt-link>
      </nav>
    </el-header>
    <nuxt />
  </div>
</template>

<style>
.the-header__nav {
  display: flex;
  justify-content: center;
}
.the-header__link {
  display: inline-flex;
  margin-right: 15px;
}
.the-header__link:last-of-type {
  margin-right: 0px;
}
</style>
