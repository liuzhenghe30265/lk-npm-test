# lk-npm-test

> npm 包

```
npm install lk-npm-test --save
```

### 组件内使用

```
<template>
  <div id="app">
    <lk-npm-test :msg="msg" @childFun="getChildMsgFun"></lk-npm-test>
  </div>
</template>

<script>
import LkNpmTest from 'lk-npm-test'
export default {
  name: 'app',
  data () {
    return {
      msg: 'hello'
    }
  },
  components: {
    LkNpmTest
  },
  methods: {
    getChildMsgFun () {
      this.msg = 'change msg'
    }
  }
}
</script>
```

### 全局使用

main.js

```
import LkNpmTest from 'lk-npm-test'
Vue.use(LkNpmTest)
```

.vue

```
<lk-npm-test :msg="msg" @childFun="getChildMsgFun"></lk-npm-test>
```
