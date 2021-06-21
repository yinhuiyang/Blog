<template>
  <div class="card">
    <h2 class="title">写写高斯模糊——从 CSS 模糊滤镜的白边说起</h2>
    <br>
    <div class="date">
      <el-icon class="iconfont el-icon-date" />
      &nbsp;
      <span>2020-10-18</span>
    </div>
    <div class="preface">
      <h2>序言</h2>
      <el-divider />
      <p>通常我们可以很容易地使用 PhotoShop 中的「高斯模糊」来模糊图片。</p>
      <p>
        这也是一种很好的艺术效果，苹果惯用的毛玻璃效果本质便是高斯模糊，而我们将图片模糊后作为网站背景，既减小了图片的体积，也能别有一番风味。（譬如咱站点的背景也是高斯模糊后的产物。）
      </p>
      <img src="../assets/images/blur-source-image.jpg" alt="">
      <p>
        而 CSS3 提供了滤镜
        filter/backdrop-filter，其中的模糊功能同样也是高斯模糊。（Canvas 中的
        filter 亦是如此。）
      </p>
      <p>只是当我们为图片背景添加 CSS 滤镜时，便会出现不和谐的白边。</p>
      <p>
        虽然有一些奇技淫巧（比如放大图片再截去模糊的边）去解决，但皆治标不治本，我们不妨借此机会探究一下高斯模糊，并尝试自己实现它
      </p>
    </div>
    <el-divider />
    <div class="articleFooter">
      <span>查看全文</span>
      <el-icon class="iconfont el-icon-d-arrow-right" />
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss">
.card {
  width: 100%;
  padding: 15px;
  box-shadow: 0 2px 12px 0 rgb(0 0 0 / 10%);
  border-radius: 4px;
  border: 1px solid #ebeef5;
  background-color: #fff;
  overflow: hidden;
  color: #303133;
  transition: 0.3s;
  margin-top: 20px;
  .title {
    color: #0078e7;
    cursor: pointer;
    font-family: 'Songti SC', 'Noto Serif SC', STZhongsong, STKaiti, KaiTi,
      Roboto, serif;
  }
  .title:hover {
    color: #db2828;
  }
  .preface {
    text-align: left;
    h2 {
      font-size: 2.2rem;
      font-weight: 300;
    }
    img {
      display: block;
      margin: 1rem auto;
      width: auto;
      height: auto;
      max-width: 92%;
      max-height: 600px;
      border-radius: 0.2rem;
      box-shadow: 0 2px 0.5rem rgb(0 0 0 / 12%);
      transition: 0.4s;
    }
    p {
      margin: 14px 0;
      line-height: 1.8;
      font-family: 'PingFang SC', 'Microsoft YaHei', Roboto, Arial, sans-serif;
    }
    .el-divider--horizontal {
      margin: 4px 0 10px 0;
    }
  }
  .articleFooter {
    text-align: right;
    cursor: pointer;
    margin-bottom: 4px;
  }
  .articleFooter:hover {
    color: #0078e7;
  }
}
.card:hover {
  box-shadow: 0 2px 12px 0 rgb(255 0 255 / 30%);
}
</style>
