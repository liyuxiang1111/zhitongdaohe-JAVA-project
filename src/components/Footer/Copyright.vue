<template>
  <div class="copyright-container">
    <div class="copyright-box">
      <div class="links">
        关于我们 | 联系我们 | 联系客服 | 商家入驻 | English Site | Contact U
      </div>
      <div class="copyright">
        地址：莆田学院 邮编：350001 电话：123456 传真：789456 邮箱: nihaoxian.com 闽ICP备08001421号闽公网安备110108007702
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Copyright'
}
</script>

<style lang="less" scroped>
.copyright-box {
  position: relative;
  text-align: center;
  padding-top: 40px;
  font: 12px/1.5 Microsoft YaHei, Heiti SC, tahoma, arial, Hiragino Sans GB, '\5B8B\4F53', sans-serif;
  height: 200px;
  width: 100%;
  background-color: #f5f5f5;
  border-bottom: 1px solid #ccc;
  .links {
    margin-bottom: 15px;
  }
  .copyright {
    line-height: 20px;
  }
}
</style>
