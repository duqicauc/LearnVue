<template>
    <div>{{state.name}}</div>
</template>

<script>
import { reactive } from 'vue'

export default {
    setup() {
        const state = reactive({ name: '阿杜'})
        return {state}
    }
}
</script>