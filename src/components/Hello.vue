<!-- 添加 "scoped" 属性使得当前样式只对当前组件有效 -->
<style scoped>
    h1 {color: #42b983;}
    button{margin-bottom:20px;}
</style>

<template>
    <img class="logo" src="../assets/logo.png">
    <div class="hello">
        <h1>{{ msg }}</h1>
        <button class="btn btn-success" v-on:click="clickFn()">send data to Input.vue</button>
    </div>
</template>

<script>
export default {
    data () {
        return {
            msg: 'Hello World'
        }
    },
    methods: {
        //广播数据
        clickFn () {
            this.$dispatch('test', this.msg)
        }
    }
}
</script>


