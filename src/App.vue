<template>
  <div id="app">
    <HeaderComponent />

    <main>
      <SectionListDisc />
    </main>
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import SectionListDisc from './components/SectionListDisc.vue';

export default {
  name: 'App',
  components: {
    HeaderComponent,
    SectionListDisc
  }
}
</script>

<style lang="scss">
@import './assets/style/common.scss';
@import './assets/style/variables.scss';

main {
  background-color: $brand_secondary_color;
  height: 100vh;
}

</style>
