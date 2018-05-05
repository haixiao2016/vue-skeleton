<template>
  <div class="main-container">
    <div class="pro-list">
      <div class="list-item skeleton"></div>
      <div class="list-item skeleton"></div>
      <div class="list-item skeleton"></div>
      <div class="list-item skeleton"></div>
    </div>
    <div class="pro-list">
      <div class="list-item skeleton"></div>
      <div class="list-item skeleton"></div>
      <div class="list-item skeleton"></div>
      <div class="list-item skeleton"></div>
    </div>
    <div class="pro-list">
      <div class="list-item skeleton"></div>
      <div class="list-item skeleton"></div>
      <div class="list-item skeleton"></div>
      <div class="list-item skeleton"></div>
    </div>
  </div>
</template>
<script>
export default {

}
</script>
<style rel="stylesheet/scss" lang="scss" scoped>
  .skeleton{
    background: rgb(194, 207, 214);
    background-image: linear-gradient(90deg,rgba(255, 255, 255, 0.15) 50%, transparent 50%);
    background-size: 50% 100%;
    background-origin:content-box;
    animation: skeleton-stripes 1s linear infinite;
  }
  @keyframes skeleton-stripes {
    from {
        background-position: top left;
    }
    to {
        background-position: top right;
    }
}
  .main-container{
    .pro-list{
      display: flex;
      width: 300px;
      margin: 0 auto;
      justify-content: space-between;
      .list-item{
        width: 50px;
        height: 50px;
        border-radius: 100%;
        margin: 10px 0;
      }
    }
  }
</style>
