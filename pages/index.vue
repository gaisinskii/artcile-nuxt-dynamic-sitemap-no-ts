<template>
  <el-container>
    <el-main>
      This is the main page. Navigate through the site using links above.
    </el-main>
  </el-container>
</template>

<script>
export default {
  head() {
    return {
      title: 'Main Page',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'Main Page description',
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
