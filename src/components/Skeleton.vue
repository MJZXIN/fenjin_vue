<template>
    <el-skeleton style="width: 240px" animated :loading="loading">
        <template #template>
            <div style="padding: 14px">
                <el-skeleton-item variant="p" style="width: 50%" />
                <div style="display: flex; align-items: center; justify-items: space-between;">
                    <el-skeleton-item variant="text" style="margin-right: 16px" />
                    <el-skeleton-item variant="text" style="width: 30%" />
                </div>
            </div>
        </template>
        <template #default>
            <span>{{ TowerNum }}</span>
        </template>
    </el-skeleton>

</template>

<script setup>
import { ref } from 'vue'
const loading = ref(false)

defineProps({
    TowerNum: Number
})

</script>