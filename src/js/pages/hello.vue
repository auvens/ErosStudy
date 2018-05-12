<template>
    <div class="container">
        <text class="title">Hello Eros</text>
        <text class="desc">一套 Vue 代码，两端原生应用。</text>
        <wxc-button text="打开test页面" @wxcButtonClicked="showEros"></wxc-button>
    </div>
</template>
<script>
import { WxcButton } from 'weex-ui'
export default {
  components: { WxcButton },
  methods: {
    // 这里给按钮添加 showEros 事件来跳转
    showEros() {
      this.$router.open({
        name: 'test'
      })
    }
  }
}
</script>
<style scoped>
.container {
  display: flex;
  flex: 1;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.title {
  font-size: 100px;
}
.desc {
  font-size: 30px;
}
</style>
