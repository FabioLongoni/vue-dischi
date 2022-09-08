<template>
  <div id="app">
    <HeaderComponent @search="onSearch"/>
    <MainComponent :search='searchProp'/>
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
      searchProp:'',
    }
  },
  components: {
    MainComponent,
    HeaderComponent,
  },
  methods: {
    onSearch(data) {
      this.searchProp = data;
    }
  }, 
}
</script>

<style lang="scss">
  @import './style/style.scss';
</style>
