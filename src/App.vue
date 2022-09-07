<template>
  <body>
    <div id="app">
      <HeaderComponent/>
      <MainComponent/>
    </div>
  </body>
</template>

<script>
import MainComponent from './components/MainComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';


export default {
  name: 'App',
  components: {
    MainComponent,
    HeaderComponent
}
}
</script>

<style lang="scss">
  @import './style/style.scss';
</style>
