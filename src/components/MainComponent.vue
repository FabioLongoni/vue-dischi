<template>
  <div class="container"> 
    <AlbumCard v-for="(album,i) in filteredAlbums" :key="i" 
      :poster="album.poster"
      :title="album.title"
      :author="album.author"
      :year="album.year"
    />
  </div>
</template>

<script>
import axios from 'axios';
import AlbumCard from './AlbumCard.vue';

export default {
    name: "MainComponent",
    props: {
      search: {
        type: String,
        default:'',
      }
    },
    data() {
        return {
            albumsList: [],
        };
    },
    computed: {
      filteredAlbums() {
        return this.albumsList.filter((el) => {
          const genre = el.genre;
          const find = this.search;

          if(genre.includes(find)) {
            return true;
          }

          return false;
        }) 
      }
    },
    created() {
        axios
            .get("https://flynn.boolean.careers/exercises/api/array/music")
            .then((res) => {
            this.albumsList = res.data.response;
            console.log(res.data.response);
        });
    },
    components: { AlbumCard }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .container {
    display: grid;
    grid-template-columns: repeat(5,1fr);
    gap: 2rem;
    max-width: 850px;
  }
</style>
