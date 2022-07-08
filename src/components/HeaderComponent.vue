<template>
    <header>       
            <img src="../assets/logo-small.svg" alt="Logo">
    </header>
</template>

<script>
export default {
    name: 'HeaderComponent'
}
</script>

<style lang="scss" scoped>
@import '../assets/style/variables.scss';

header {
    background-color: $brand_primary_color;
    height: 40px;
    display: flex;
    align-items: center;
    padding-left: 15px;

    img {
        width: 20px;
    }
}

</style>