<template>
  <div class="container"> 
    <DiscoCard v-for="(disco,i) in discoList" :key="i" 
      :poster="disco.poster"
      :title="disco.title"
      :author="disco.author"
      :year="disco.year"
    />
  </div>
</template>

<script>
import axios from 'axios';
import DiscoCard from './DiscoCard.vue';

export default {
    name: "MainComponent",
    data() {
        return {
            discoList: [],
        };
    },
    created() {
        axios
            .get("https://flynn.boolean.careers/exercises/api/array/music")
            .then((res) => {
            this.discoList = res.data.response;
            console.log(res.data);
        });
    },
    components: { DiscoCard }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .container {
    display: grid;
    grid-template-columns: repeat(5,1fr);
    gap: 2rem;
  }
</style>
