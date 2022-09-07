<template>
  <body>
    <div id="app">
      <MainComponent/>
    </div>
  </body>
</template>

<script>
import MainComponent from './components/MainComponent.vue';


export default {
  name: 'App',
  components: {
    MainComponent,
}
}
</script>

<style lang="scss">
  @import './style/style.scss';
</style>
