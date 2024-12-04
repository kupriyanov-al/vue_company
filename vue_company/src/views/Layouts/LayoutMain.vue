<script setup>
import AppHeaderNav from '@/components/AppHeaderNav.vue';
import AppAsideNav from '@/components/AppAsideNav.vue';

</script>

<template>
    <div class="container">
        <div class="common-layout">
            <el-container class="el-container ">
                <el-header>
                    <AppHeaderNav></AppHeaderNav>
                </el-header>

                <el-container>
                    <el-aside width="60px">
                            <AppAsideNav></AppAsideNav>
                    </el-aside>
                    <el-container>
                        <el-main>Main</el-main>
                        <el-footer>Footer</el-footer>
                    </el-container>
                </el-container>
            </el-container>
        </div>
    </div>


</template>

<style scoped lang="scss">
@import '@/assets/main.scss';

.container {

    max-width: 90%;
    margin: 0 auto;

}

.el-header{
    --el-header-padding: 0 0;
}

.common-layout {
    height: 100vh;
}

.el-container {
    min-height: 100%;
    
}

.el-aside {
    border-right: 1px solid rgb(219, 219, 219);
    background: #fdfdfd;  
}

</style>