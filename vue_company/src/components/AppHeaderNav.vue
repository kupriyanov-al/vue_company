<script setup>


</script>

<template>
    <div class="header_main">
        <div class="logo">LOGO</div>
        <div class="nav__menu">
            <div class="nav__menu-item">Контроллеры</div>
            <div class="nav__menu-item">Станции управления</div>
            <div class="nav__menu-item">Расходомеры</div>
            <div class="nav__menu-item nav__auth">
                <div class="nav__auth-item">Login</div>
            </div>
        </div>
    </div>

</template>

<style scoped lang="scss">
@import '../assets/main.scss';

.header_main {
    display: flex;
    justify-content: space-between;
    background: #ffffff;
    align-items: center;
    border-bottom: 2px solid $border-color;   
}

.nav__menu {
    display: flex;
    gap: 15px;
    text-transform: uppercase;
   
    &-item {
        padding: 20px 15px;

    };

    &-item:hover {
        color: #6b6b6b;
        transition: 500ms;
        background: #e9e9e9;
    };
}

.nav__auth {
    margin:0 50px;
}

.header_main {
    
}

.logo {
    margin-left: 20px;
}

</style>