/* eslint-disable nuxt/require-func-head */
<template>
  <el-row type="flex" justify="center">
    <el-col :xs="24" :sm="20" :md="18" :lg="12">
      <app-blog v-for="blog in 3" :key="blog" />
    </el-col>
  </el-row>
</template>
<script>
import AppBlog from '@/components/main/blog'
export default {
  // eslint-disable-next-line nuxt/require-func-head
  head: {
    title: 'Главная страница'
  },
  components: {
    AppBlog
  }
}
</script>
