<template>
  <div class="container">
    <Category title="美食">
      <img src="../src/assets/shaokao.jpeg" alt="">
    </Category>
    <Category title="游戏">
      <ul>
        <li v-for="(g,index) in games" :key="index">{{ g }}</li>
      </ul>
    </Category>
    <Category title="电影">
      <video controls src="../src/assets/shipin.mp4" alt=""></video>
    </Category>
  </div>
</template>

<script>
import Category from './components/Category'

export default {
  name: 'App',
  components: {
    Category
  },
  data() {
    return {
      foods:['火锅','烧烤','小龙虾','牛排'],
      games:['红色警戒','穿越火线','劲舞团','超级玛丽'],
      films:['《教父》','《拆弹专家》','《你好，李焕英》','《嗯嗯》'],
    }
  }
}
</script>

<style scoped>
  .container{
    display: flex;
    justify-content: space-around;
  }
  img{
    width: 100%;
  }
  video{
    width: 100%;
  }
</style>
