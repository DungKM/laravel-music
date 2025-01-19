<template>
  <div class="container-fluid">
    <div class="row text-white" style="background-color: #0c713d; padding: 1rem">
      <div class="col-1 d-flex d-sm-none align-items-center justify-content-center">
        <span @click="showDrawer">X</span>
      </div>
      <div class="col-10 col-sm-9 d-flex align-items-center justify-content-center justify-content-sm-start">
        <img src="https://tse2.mm.bing.net/th?id=OIP.XrGVljajcLZhvJGUD-Sc7gHaE7&pid=Api&P=0&h=180" alt="Logo"
          style="width: 50px; height: 50px">
        <span class="d-none d-sm-flex">Quản trị</span>
      </div>
      <div class="col-sm-3 d-none d-sm-flex align-items-center justify-content-sm-end">
        <span>Admin</span>
      </div>
      <div class="col-1 d-flex d-sm-none align-items-center justify-content-center">
        <span @click="showDrawerUser">X</span>
      </div>
    </div>
  </div>
  <a-drawer v-model:open="open" class="custom-class" root-class-name="root-class-name" :root-style="{ color: 'blue' }"
    style="color: red" title="Danh mục" placement="right" @after-open-change="afterOpenChange">
    <p>Some contents...</p>
    <p>Some contents...</p>
    <p>Some contents...</p>
  </a-drawer>
  <a-drawer v-model:open="open_user" class="custom-class" root-class-name="root-class-name"
    :root-style="{ color: 'blue' }" style="color: red" title="Admin" placement="right"
    @after-open-change="afterOpenChange">
    <p>Some contents...</p>
    <p>Some contents...</p>
    <p>Some contents...</p>
  </a-drawer>
</template>
<script setup>
import { ref } from 'vue';
const open = ref(false);
const open_user = ref(false);
const afterOpenChange = bool => {
  console.log('open', bool);
};
const showDrawer = () => {
  open.value = true;
};
const showDrawerUser = () => {
  open_user.value = true;
};
</script>