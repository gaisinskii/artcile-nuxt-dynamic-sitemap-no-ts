<template>
  <el-container>
    <el-main>
      <ul>
        <li v-for="(album, index) in albums" :key="index">
          {{ album.title }}
        </li>
      </ul>
    </el-main>
  </el-container>
</template>

<script>
export default {
  async asyncData({ $axios }) {
    const response = await $axios.$get('/albums')
    return {
      albums: response,
    }
  },
  data() {
    return {
      albums: [],
    }
  },
  head() {
    return {
      title: 'All Albums Page',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'All Users Page description',
        },
      ],
    }
  },
}
</script>

<style>
.page__link {
  display: inline-flex;
}
</style>
