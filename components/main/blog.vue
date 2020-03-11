<template>
  <el-card
    :body-style="{ padding:0 }"
    shadow="hover"
    class="post"
  >
    <header slot="header" class="post-header">
      <h3>Post title</h3>
      <small>
      <i class="el-icon-time"></i>
      {{ new Date().toLocaleString() }}
      </small>
    </header>

    <div class="post-body">
      <img
        src="https://cdn.pixabay.com/photo/2019/08/17/20/46/dolomites-4412914_960_720.jpg"
        alt=""
        class="post-img"
      >
    </div>
    <footer class="post-footer">
      <el-button @click="openPost" round>
        Open
      </el-button>
      <span><i class="el-icon-message" />12</span>
    </footer>
  </el-card>
</template>

<script>
export default {
  methods: {
    openPost () {
      const id = '2'
      this.$router.push(`post/${id}`)
    }
  }
}
</script>

<style lang="scss" scoped>
.post{
  margin-bottom: 1.5em;
}
.post-header{
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.post-body{
  //margin-bottom: 1rem;
}
.post-img{
  width: 100%;
  height: auto;

}
.post-footer{
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem;
}
</style>
