<script setup>
import { RouterLink, RouterView } from 'vue-router'
import LayoutMain from './views/Layouts/LayoutMain.vue';

</script>

<template>
  <div class="wrapper">
    <layout-main></layout-main>
  </div>
</template>

<style scoped lang="scss">

.wrapper {
	min-width: 100%;
  height: 400px;

}

</style>
