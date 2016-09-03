<template>
    <!-- lazy 在 "change" 而不是 "input" 事件中更新 -->
    <input type="text" class="form-control" v-model="message" placeholder="from Input.vue" v-if="message" lazy>
</template>

<script>
export default {
    data () {
        return {
            message: '',
        }
    },
    events: {
        //接受来自Hello.vue组件的数据
        send (msg) {
            this.message += ' ' + msg;
        }
    }}
</script>


