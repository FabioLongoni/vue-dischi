<template>
  <div class="container"> 
    <div v-for="disco,i in discoList" :key="i">
      {{disco}}
    </div>   
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'MainComponent',
  data() {
    return {
      discoList: [],
    }
  },
  created() {
    axios
      .get('https://flynn.boolean.careers/exercises/api/array/music')
      .then((res) => {
        this.discoList = res.data;
        console.log(res.data);
      });
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
