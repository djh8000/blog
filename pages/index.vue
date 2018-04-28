<template>
  <section class="container">
    <canvas id="lizi-cv"></canvas>
    <canvas id="zhihu-cv"></canvas>
    <div>
      <app-logo/>
      <h1 class="title">
        djh-blog
      </h1>
      <h2 class="subtitle">
        董军浩的个人网站
      </h2>
      <h3>正在努力建设中...</h3>
    </div>
  </section>
</template>

<script>
import AppLogo from '~/components/AppLogo.vue'
import zhihu from '~/plugins/zhihu-cv.js'
import lizi from '~/plugins/lizi-cv.js'

export default {
  components: {
    AppLogo
  },
  mounted () {
    this.$nextTick(function () {
      zhihu('zhihu-cv')
      lizi('lizi-cv')
    })
  }
}
</script>

<style>
canvas{
  position: fixed;
  top: 0;
  left: 0;
  z-index: -1;
}
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
