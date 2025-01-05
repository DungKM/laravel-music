<template>
    <TheHeader />
    <div class="container-fuild">
        <div class="row">
            <div class="col-sm-3 d-none d-sm-flex">
                side bar
            </div>
            <div class="col-sm-12">
                <router-view></router-view>
            </div>
        </div>
    </div>
</template>
<script>
import TheHeader from '../components/TheHeader.vue';

export default {
    components: {
        TheHeader
    }
}
</script>