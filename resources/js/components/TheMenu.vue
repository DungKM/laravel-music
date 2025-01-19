<template>
    <a-menu v-model:openKeys="state.openKeys" v-model:selectedKeys="state.selectedKeys" mode="inline" :items="items">
        <a-menu-item key="admin-users">
            <router-link :to="{ name: 'admin-users' }">Tài khoản</router-link>
        </a-menu-item>
        <a-menu-item key="admin-roles">
            <router-link :to="{ name: 'admin-roles' }">Vai trò</router-link>
        </a-menu-item>
        <a-menu-item key="admin-settings">
            <router-link :to="{ name: 'admin-settings' }">Cài đặt</router-link>
        </a-menu-item>
    </a-menu>
</template>
<script setup>
import { reactive, watch, h } from 'vue';
const state = reactive({
    selectedKeys: ['admin-users'],
    openKeys: [],
});
watch(
    () => state.openKeys,
    (_val, oldVal) => {
        state.preOpenKeys = oldVal;
    },
);
</script>