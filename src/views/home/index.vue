<template>
  <div class="home">
    <div class="gaoshi" />
    <el-scrollbar
      :native="false"
      wrap-style=""
      wrap-class=""
      view-class=""
      view-style=""
      :noresize="false"
      tag="section"
      style="height: 100%"
    >
      <div class="container">
        <aside>
          <UserCenter />
        </aside>
        <main>
          <section>
            <card />
            <card />
            <card />
          </section>
        </main>
        <footer />
      </div>
    </el-scrollbar>
  </div>
</template>

<script>
import Card from '@/components/card'
import UserCenter from '@/components/userCenter'
export default {
  name: 'Home',
  components: {
    Card,
    UserCenter
  }
}
</script>

<style lang="scss">
.home {
  height: 100%;
  .el-scrollbar__wrap {
    overflow-x: hidden;
  }
  .gaoshi {
    height: 100%;
    width: 100%;
    background-image: url('../../assets/images/blur-source-image.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    filter: blur(200px);
    position: fixed;
    top: 0;
    left: 0;
    z-index: 1;
  }
  .container {
    z-index: 2;
    position: relative;
    padding-bottom: 20px;
    aside {
      width: 300px;
      background: #ffffff;
      height: 100%;
      display: inline-block;
      position: fixed;
      top: 0;
      left: 0;
      text-align: center;
      z-index: 10;
      transition-property: all;
      transition-duration: 0.3s;
      transition-delay: 0s;
      box-shadow: 0 0 2px rgb(0 0 0 / 20%);
      border-right: 1px solid #cccccc;
    }
    aside:hover {
      box-shadow: 0 0 15px rgb(255 0 255 / 50%);
    }
    main {
      padding-left: 300px;
    }
    section {
      width: 900px;
      margin: 0 auto;
    }
  }
}
</style>
