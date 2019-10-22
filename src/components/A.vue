<template>
  <div>
    A组件:
    <span>{{elementValue}}</span>
    <input type="button" value="点我传送值" @click="elementByValue">
  </div>
</template>
<script>
  // 引入公共的MiddleStore，来做为中间传达的工具
  import MiddleStore from '../views/middle-store.js'
  export default {
    data () {
      return {
        elementValue: 4
      }
    },
    methods: {
      elementByValue: function () {
        MiddleStore.$emit('val', this.elementValue)
      }
    }
  }
</script>