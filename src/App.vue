<style>
    #app {color: #2c3e50;padding:100px 0;}
    .logo {width: 100px;height: 100px}
</style>

<template>
    <div class="col-md-4 col-md-offset-4 text-center" id="app">        
        <hello></hello>        
        <text></text>
    </div>
</template>

<script>
import Hello from './components/Hello.vue'
import Input from './components/Input.vue'

export default {
    data () {
        return{
            message : []
        }
    },
    events: {
        //父组件派发数据
        'test': function (msg) {
            this.$broadcast('send', msg)
        }
    },    
    components: {
        'hello': Hello,
        'text': Input
    }
}
</script>