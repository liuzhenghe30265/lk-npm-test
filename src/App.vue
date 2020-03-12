<template>
  <div>
    <Main :msg="msg" @childFun="getChildMsgFun"></Main>
  </div>
</template>

<script>
import Main from './components/Main'
export default {
  name: 'app',
  data () {
    return {
      msg: 'lk-npm-test'
    }
  },
  components: {
    Main
  },
  methods: {
    // 接收父组件传值
    getChildMsgFun (msg) {
      this.msg = msg
    }
  }
}
</script>

<style lang="scss">
</style>
