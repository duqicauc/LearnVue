<template>
    <!-- 通过大括号显式state下的name的值 -->
    <div>{{state.name}}</div>
    
    <!-- v-text指令，更新元素的textContent -->
    <span v-text="state.name"></span>
</template>

<script>
// Vue3通过import的形式引入构造双向绑定数据的reactive方法
import { reactive } from 'vue'

export default {
    setup() {
        // 构造响应式数据state
        const state = reactive({ name: '阿杜'})
        // 必须通过return返回，目的是让模板可以获得返回的属性，之类可以是方法和变量
        return {state}
    }
}
</script>