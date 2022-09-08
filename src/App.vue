<template>
  <div id="app">
    <HeaderComponent @search="onChange"/>
    <MainComponent :search='changeGenre'/>
  </div> 
</template>

<script>
import MainComponent from './components/MainComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import "@fontsource/montserrat";

export default {
  name: 'App',
  data() {
    return {
      changeGenre:'',
    }
  },
  components: {
    MainComponent,
    HeaderComponent,
  },
  methods: {
    onChange(data) {
      this.changeGenre = data;
    }
  }, 
}
</script>

<style lang="scss">
  @import './style/style.scss';
</style>
