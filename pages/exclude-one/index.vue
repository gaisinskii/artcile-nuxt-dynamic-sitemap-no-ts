<template>
  <el-container>
    <el-main> Page #1 to exclude from sitemap generation </el-main>
  </el-container>
</template>

<script>
export default {
  head() {
    return {
      title: 'Exclude Page',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Exclude Page description',
        },
      ],
    }
  },
}
</script>
