<template>
    <div v-if="show" class="sync_box">
        <p>默认初始值是true,显示</p>
        <button @click="close">关闭</button>
    </div>
</template>

<script>
export default {
    props: ['show'],
    data() {
        return {}
    },
    methods: {
        close() {
            this.$emit('update:show', false)
        }
    }
}
</script>

<style lang='scss'>
.sync_box {
    width: 200px;
    border: 1px solid #eee;
    margin: 0 auto;
    padding: 20px 0;
}
</style>