<template>
  <article class="post">
    <header class="post-header">
      <div class="post-title">
        <h1>Post title</h1>
        <nuxt-link to="/">
          <i class="el-icon-back"></i>
        </nuxt-link>
      </div>

      <div class="post-info">
        <small>
          <i class="el-icon-time"></i>
          {{ new Date().toLocaleString() }}
        </small>
        <small>
          <i class="el-icon-view"></i>
          32
        </small>
      </div>
      <div class="post-img">
        <img src="https://cdn.pixabay.com/photo/2019/08/17/20/46/dolomites-4412914_960_720.jpg" alt />
      </div>
    </header>
    <main class="post-content">
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugit reiciendis nostrum, ratione laborum maiores voluptates. Beatae magni molestias corrupti ratione.</p>
    </main>
    <footer></footer>
  </article>
</template>

<script>
export default {
  validate({ params }) {
    return Boolean(params.id);
  }
};
</script>
<style lang="scss" scoped>
.post {
  max-width: 600px;
  margin: 0 auto;
}
.post-title{
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1rem;
}
.post-info{
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 0.5rem;
}
.post-img img{
  width: 100%;
  height: auto;
}
.post-header{
  margin-bottom: .5rem;
}
.post-content{
  margin-bottom: 2rem;
}
</style>
