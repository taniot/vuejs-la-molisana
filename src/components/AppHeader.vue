<script>
import AppLogo from './AppLogo.vue';
import AppNav from './AppNav.vue';

export default {
    name:'AppHeader',
    components: {
        AppLogo,
        AppNav
    }
}
</script>

<template>
    <header>
        <!-- Componente Logo-->
        <AppLogo></AppLogo>
         <!-- Componente Menu-->
        <AppNav></AppNav>
    </header>
</template>

<style lang="scss" scoped>
header {
    text-align:center;
}
</style>