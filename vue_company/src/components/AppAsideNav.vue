<script setup>


</script>

<template>
    <div class="aside-menu">

        <div class="aside-menu__item">
            <el-icon :size="30">
                <House />
            </el-icon>
        </div>
        <div class="aside-menu__item">
            <el-icon :size="30">
                <Grid />
            </el-icon>
        </div>
        <div class="aside-menu__item">
            <el-icon :size="30">
                <setting />
            </el-icon>
        </div>

    </div>

</template>

<style  lang="scss" scoped>
@import '@/assets/main.scss';

// -------------
.aside-menu {
    margin-top: 30px;
    display: flex;
    flex-direction: column;
    
    justify-content: center;
    align-items: center;
    
}



.aside-menu__item {
    padding: 10px;
}

.aside-menu__item:hover {
    color: #6b6b6b;
        transition: 500ms;
        background: #e9e9e9; 
    }
</style>