<template>
  <div>
    父组件:
    <input type="text" v-model="name">
    <br>
    <br>
    <!-- 引入子组件 -->
    <home-child :inputName="name"></home-child>
    <hr>
    <A></A> 
    <B></B>
  </div>
</template>
<script>
  import HomeChild from '../components/home-child'
  import A from '../components/A.vue'
  import B from '../components/B.vue'
  export default {
    components: {
      HomeChild,
      A,
      B
    },
    data () {
      return {
        name: ''
      }
    }
  }
</script>