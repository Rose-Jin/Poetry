<template>
  <div id="app">
    <h3>案例：折叠面板</h3>
    <div>
      <div class="title">
        <h4>静夜思</h4>
        <span class="btn" @click='isShow=!isShow'>
          {{isShow?'收起':'展开'}}
        </span>
      </div>
      <div class="container" v-show='isShow'>
        <p>床前明月光，</p>
        <p>疑是地上霜。</p>
        <p>举头望明月，</p>
        <p>低头思故乡。</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
    isShow:true
  }
  }
}
</script>

<style lang="less">
body {
  background-color: #ccc;
  #app {
    width: 400px;
    margin: 20px auto;
    background-color: #fff;
    border: 4px solid blueviolet;
    border-radius: 1em;
    box-shadow: 3px 3px 3px rgba(0, 0, 0, 0.5);
    padding: 1em 2em 2em;
    h3 {
      text-align: center;
    }
    .title {
      display: flex;
      justify-content: space-between;
      align-items: center;
      border: 1px solid #ccc;
      padding: 0 1em;
    }
    .title h4 {
      line-height: 2;
      margin: 0;
    }
    .container {
      border: 1px solid #ccc;
      padding: 0 1em;
    }
    .btn {
      /* 鼠标改成手的形状 */
      cursor: pointer;
    }
  }
}
</style>