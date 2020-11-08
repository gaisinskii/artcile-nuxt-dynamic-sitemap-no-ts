<template>
  <el-container>
    <el-main>
      <table class="page__table">
        <thead>
          <tr>
            <th>ID</th>
            <th>User Name</th>
            <th>User Alias</th>
            <th>Edit</th>
          </tr>
        </thead>
        <tbody>
          <tr
            v-for="(user, index) in users"
            :key="index"
            class="page__table-row"
          >
            <td>{{ user.id }}</td>
            <td>{{ user.name }}</td>
            <td>{{ user.username }}</td>
            <td>
              <nuxt-link
                class="page__link"
                :to="{
                  name: 'users-id',
                  params: {
                    id: user.id,
                  },
                }"
              >
                <el-button type="primary" icon="el-icon-edit" circle />
              </nuxt-link>
            </td>
          </tr>
        </tbody>
      </table>
    </el-main>
  </el-container>
</template>

<script>
export default {
  async asyncData({ $axios }) {
    const response = await $axios.$get('/users')
    return {
      users: response,
    }
  },
  data() {
    return {
      users: [],
    }
  },
  head() {
    return {
      title: 'All Users Page',
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
.page__table {
  width: 550px;
  margin: 0 auto;
  text-align: left;
  border-collapse: separate;
  border-spacing: 0 1em;
}
</style>
