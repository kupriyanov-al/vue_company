<script setup>
import AppHeaderNav from '@/components/AppHeaderNav.vue';

</script>

<template>
    <div class="container">
        <div class="common-layout">
            <el-container class="el-container ">
                <el-header>
                    <AppHeaderNav></AppHeaderNav>
                </el-header>

                <el-main>Main</el-main>
                <el-footer>Footer</el-footer>
            </el-container>
        </div>
    </div>


</template>

<style scoped lang="scss">
.container {

    max-width: 90%;
    margin: 0 auto;

}

.common-layout {
    height: 100vh;
}

.el-container {
    min-height: 100%;
}



</style>