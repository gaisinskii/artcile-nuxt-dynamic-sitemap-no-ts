<template>
  <el-container>
    <el-main>
      <ul>
        <li v-for="(todo, index) in todos" :key="index">
          <el-checkbox v-model="todo.completed" disabled />
          {{ todo.title }}
        </li>
      </ul>
    </el-main>
  </el-container>
</template>

<script>
export default {
  async asyncData({ $axios }) {
    const response = await $axios.$get('/todos')
    return {
      todos: response,
    }
  },
  data() {
    return {
      todos: [],
    }
  },
  head() {
    return {
      title: 'All Todos Page',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'All Todos Page Page description',
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
