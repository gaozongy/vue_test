<!--<template>-->
<!--  <div>-->
<!--    <button @click="isShow = !isShow">显示/隐藏</button>-->
<!--    <h1 v-show="isShow" class="come">你好啊!</h1>-->
<!--  </div>-->
<!--</template>-->

<!--<script>-->
<!--  export default {-->
<!--    name:'Test',-->
<!--    data() {-->
<!--      return {-->
<!--        isShow:true-->
<!--      }-->
<!--    }-->
<!--  }-->
<!--</script>-->

<!--<style scoped>-->
<!--  h1{-->
<!--    background-color: orange;-->
<!--  }-->

<!--  .come{-->
<!--    animation: atguigu 1s;-->
<!--  }-->

<!--  .go{-->
<!--    animation: atguigu 1s reverse;-->
<!--  }-->

<!--  @keyframes atguigu {-->
<!--    from{-->
<!--      transform: translateX(-100%);-->
<!--    }-->
<!--    to{-->
<!--      transform: translateX(0px);-->
<!--    }-->
<!--  }-->
<!--</style>-->


<template>
  <div>
    <button @click="isShow = !isShow">显示/隐藏</button>
    <transition name="hello" appear>
      <h1 v-show="isShow" class="come">你好啊!</h1>
    </transition>
  </div>
</template>

<script>
export default {
  name:'Test',
  data() {
    return {
      isShow:true
    }
  }
}
</script>

<style scoped>
h1{
  background-color: orange;
}

.hello-enter-active{
  animation: atguigu 1s;
}

.hello-leave-active{
  animation: atguigu 1s reverse;
}

@keyframes atguigu {
  from{
    transform: translateX(-100%);
  }
  to{
    transform: translateX(0px);
  }
}
</style>