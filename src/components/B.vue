<template>
    <div>
        B组件:
        <input type="button" value="点我自己加" @click="getData">
        <span>{{name}}</span>
    </div>
</template>
<script>
    import MiddleStore from '../views/middle-store.js'
    export default {
        data () {
            return {
                name: 0
            }
        },
        mounted: function () {
            var vm = this
            // 用$on事件来接收参数
            MiddleStore.$on('val', (data) => {
                console.log(data)
                vm.name = data
            })
        },
        methods: {
            getData: function () {
                this.name++
            }
        }
    }
</script>